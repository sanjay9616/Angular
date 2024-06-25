<h1>Angular Router</h1>

Angular routing is a mechanism that allows you to navigate between different components in a single-page application (SPA) without triggering a full page reload. It helps organize and structure your application by associating different views (components) with specific URLs.

<h3>Key Terms Explained</h3>

1. **Route**: A route in Angular is a mapping between a URL path and a component. When a user navigates to a specific URL, the associated component is rendered.
2. **Router**: The Angular Router is a powerful module that facilitates navigation and provides a way to configure routes in your application.
3. **Router Outlet**: The <router-outlet> directive is a placeholder where the routed component will be displayed. It acts as the container for the component associated with the current route.
4. **Route Configuration**: This is where you define your application's routes. The configuration includes the path, component to be displayed, and optional data.
5. **RouterLink**: The [routerLink] directive is used in templates to create links for navigating to specific routes. It's a handy way to navigate without writing out the full URL.
6. **RouterModule**: The RouterModule is an Angular module that provides the necessary directives, services, and functionality for implementing routing in an application.

`Let's Break It Down...`

<h2>1. Setting Up Routes</h2>

```ts
// app-routing.module.ts

import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { HomeComponent } from './home.component';
import { AboutComponent } from './about.component';
import { ViewComponent } from './post/view/view.component';

const routes: Routes = [
    { path: '', component: HomeComponent },
    { path: 'about', component: AboutComponent },
    { path: 'post/:postId/view', component: ViewComponent },
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule],
})
export class AppRoutingModule {}
```
Here, we define routes for the home and about components. The empty path '' represents the default route.

<h2>2. Adding the Router Outlet</h2>

```html
<!-- app.component.html -->

<div>
  <h1>Angular Routing Blog 📚</h1>
  <nav>
    <a [routerLink]="'/'">Home</a>
    <a [routerLink]="'/about'">About</a>
  </nav>
</div>
<router-outlet></router-outlet>
```
The <router-outlet> serves as a placeholder where the content of the routed component will be displayed.

<h2>3. Navigating with RouterLink</h2>

```html
<!-- home.component.html -->

<p>Welcome to the Home Component!</p>
<a [routerLink]="'/about'">Visit About Page</a>

//Dynamic routing
<a href="#" [routerLink]="['/post/',post.id,'view']" class="btn btn-info">View</a>
```
Clicking the link triggers navigation to the 'about' route.

<h2>Accessing query parameters and fragments</h2>

```ts
import { Component, OnInit } from '@angular/core';
import {  ActivatedRoute } from '@angular/router';

@Component({
  selector: 'app-about',
  templateUrl: './about.component.html',
  styleUrls: ['./about.component.css']
})

export class AboutComponent implements OnInit {

constructor(private route: ActivatedRoute) { }

ngOnInit(): void {
    console.log(this.route.snapshot.queryParams);
    console.log(this.route.snapshot.fragment);
    console.log(this.route.snapshot.params);
  }
}
```
```ts
ngOnInit(): void {
    this.activatedRoute.params.subscribe((routeParams: any) => {
      this.params = routeParams?.itemId;
    })
  }
```

<h1>9 ways to pass data through Angular RouterState</h1>

<h3>1. URL or route parameters</h3>

Consider a route /pizza. To fetch details of a particular pizza, the route must look like /pizza/1 or /pizza/2, where the numbers 1 and 2 refer to the unique ID of a pizza. However, this number varies depending on which pizza the user clicked on and, thus, chose to order. Such dynamic values are handled using route parameters (1 and 2 are known as URL or route parameters).

Route parameters can be passed in just two simple steps:

- Define the route
- Define the navigation

**a. Define the route**: The parameter is defined by adding a forward slash (/), followed by a colon (:) and a placeholder. Consider the example below:

```ts
{ path: ’pizza/:id’, component: PizzaComponent }
```

The above path matches all the pizzas with URLs such as `/pizza/1`, `/pizza/2`, and so on.

In case of multiple parameters, add one more /,: and placeholder. See the example given below:

```ts
{ path: ’pizza/:id/:id1/:id2’,component: PizzaComponent }
```

**b. Define the navigation**: Consider the URL:/pizza/:id that fetches details of a particular pizza by its unique ID. The base path (pizza) and the route parameter (id) must be provided to the routerLink directive as shown below:

```html
<a [routerLink]="[‘/pizza’,pizzaObject.pizzaID]">{{pizzaObject.name}}</a>
```

‘pizza’ and ‘pizzaID’ are passed as the first parameter and second parameter, respectively, to the routerLink array. Thus, pizzaID is dynamically taken from the pizza object, pizzaObject.


1. Query parameters using router. navigate
2. Query parameters using queryParamsHandling
3. Query parameters using RouterLink
4. URL fragment
5. Data property
6. RouterLink for dynamic data
7. Dynamic data using navigateByURL
8.  Wildcard routes

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
