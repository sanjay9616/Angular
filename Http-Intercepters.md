<h1>Http Intercepters</h1>

- HTTP Interceptors are a concept in web development and server-side programming, typically associated with web frameworks and libraries.
- These interceptors allow developers to intercept and handle HTTP requests and responses globally within an application.
- HTTP Interceptors in Angular are classes that implement the HttpInterceptor interface.
- They can be used to perform various tasks related to HTTP requests and responses, such as adding headers, handling errors, modifying the request or response data, logging, authentication, etc.
- HttpInterceptor defines a single method called intercept, which takes two parameters: the HttpRequest and the HttpHandler.
<img src="https://miro.medium.com/v2/resize:fit:700/1*jQqkshIeWBjd1T13LO4E8w.png" alt="not found"></img>

```ts
// app.module.ts
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
import { HttpClientModule, HTTP_INTERCEPTORS } from '@angular/common/http';
import { NgHttpLoaderModule } from 'ng-http-loader';
import { AppRoutingModule } from './app-routing.module';
import { AppMaterialModule } from './material-module'
import { AppComponent } from './app.component';
import { AuthInterceptor } from './modules/_shared/_interceptors/auth.interceptor';
import { ReactiveFormsModule } from '@angular/forms';
@NgModule({
    declarations: [AppComponent],
    imports: [
        BrowserModule,
        BrowserAnimationsModule,
        HttpClientModule,
        AppRoutingModule,
        AppMaterialModule,
        ReactiveFormsModule,
        NgHttpLoaderModule.forRoot(),
    ],
    providers: [
        {
            provide: HTTP_INTERCEPTORS,
            useClass: AuthInterceptor,
            multi: true
        },
    ],
    bootstrap: [AppComponent]
})

export class AppModule { }
```
```ts
import { Injectable } from "@angular/core";
import { HttpEvent, HttpInterceptor, HttpHandler, HttpRequest, } from "@angular/common/http";
import { AuthService } from "../../auth/_services/auth.service";
import { Observable } from "rxjs";

@Injectable()
export class AuthInterceptor implements HttpInterceptor {

    private application: string = "EOC";

    constructor(private authService: AuthService) { }

    intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
        if (req.url) {
            let reqHeader: HttpRequest<any>;
            if (req.url.includes(this.authService.getSalesOpsBaseUrl())) {
                const token: string = this.authService.getSalesOpsToken();
                reqHeader = req.clone({
                    headers: req.headers
                        .append(AuthService.SALES_OPS_TOKEN, token || '')
                });
            } else {
                const token: string = this.authService.getToken() ? `Bearer ${this.authService.getToken()}` : "";
                const userId: any = this.authService.getUserId();
                const companyId: any = this.authService.getCompanyId();
                const applicationId: any = this.authService.getApplicationId();
                const branchId: any = this.authService.getBranchId();
                reqHeader = req.clone({
                    headers: req.headers
                        .append(AuthService.AUTH_TOKEN, token || '')
                        .append(AuthService.AUTHORIZATION_TOKEN, token)
                        .append(AuthService.AUTH_USER_ID, userId || '')
                        .append(AuthService.AUTH_BRANCH_ID, branchId || '')
                        .append(AuthService.AUTH_COMPANY_ID, companyId || '')
                        .append(AuthService.AUTH_APPLICATION_ID, applicationId || '')
                        .append(AuthService.APPLICATION, this.application || '')
                });
            }
            return next.handle(reqHeader);
        } else {
            return next.handle(req);
        }
    }
}
```

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
