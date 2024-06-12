<h1>HttpClient Module in Angular</h1>

- Making basic GET, POST, PUT, PATCH or DELETE requests is very similar to what you’re used to with the old Http API. One major difference is that a JSON response is expected by default, so there’s no need to explicitly parse the JSON response anymore.
- First, you’ll need to import HttpClientModule from @angular/common/http in your app module:

```ts
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { HttpClientModule } from '@angular/common/http';

import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  imports: [
    BrowserModule,
    HttpClientModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule {}
```

And then you can use the HttpClient just as you would normally:

```ts
// prService
import { Injectable } from '@angular/core';
import { PARAMS } from '@app/config/params';
import { ApiService } from '@app/services/api.service';
import { environment as env } from '../../../environments/environment'

@Injectable({
  providedIn: 'root'
})

export class PrService {

  constructor(private apiService: ApiService) { }

  getPRDashboardGloablFilterList() {
    let url = `${env.buyerInternal.baseUrl}${PARAMS.BUYER_INTERNAL.MODULES.RFQ.GET_PR_DASHBOARD_GLOBAL_FILTERS.URL}`;
    return this.apiService.get(url);
  }
}
```

```ts
import { Injectable } from '@angular/core';
import { Observable } from "rxjs";
import { HttpClient, HttpRequest, HttpHeaders, HttpErrorResponse } from "@angular/common/http";
import { throwError } from "rxjs";
import { tap } from "rxjs/operators";
import { AlertMessageService } from './alert-message.service';
import { AppProgressBarService } from './app-progress-bar.service';
import { PARAMS } from '@app/config/params';
import * as lodash from 'lodash';
import { MESSAGES } from '@app/config/messages';
import { AuthService } from '@app/services/auth.service';

@Injectable({
  providedIn: 'root'
})
export class ApiService {
  constructor(private http: HttpClient, private appProgressBarService: AppProgressBarService,
    private alertMessageService: AlertMessageService) { }

  public get(url: string, options?: any): Observable<any> {
    return this.http
      .get(this.createUrl(url), options)
      .pipe(tap(this.handleSuccess, this.handleError));
  }

  public post(url: string, data: any, options?: any): Observable<any> {
    return this.http
      .post(this.createUrl(url), data, options)
      .pipe(tap(this.handleSuccess, this.handleError));
  }

  public put(url: string, data: any): Observable<any> {
    return this.http
      .put(this.createUrl(url), data)
      .pipe(tap(this.handleSuccess, this.handleError));
  }

  public delete(url: string) {
    return this.http
      .delete(this.createUrl(url))
      .pipe(tap(this.handleSuccess, this.handleError));
  }

  private createUrl(url: string): string {
    return url;
  }

  private handleSuccess(result: any) {
    return result;
  }

  private handleError(error: HttpErrorResponse) {
    return throwError(error);;
  }
}
```

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
