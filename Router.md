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

<h2>4. Accessing query parameters and fragments</h2>

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

**b. Define the navigation**: Consider the `URL:/pizza/:id` that fetches details of a particular pizza by its unique ID. The base path (pizza) and the route parameter (id) must be provided to the routerLink directive as shown below:

```html
<a [routerLink]="[‘/pizza’,pizzaObject.pizzaID]">{{pizzaObject.name}}</a>
```

`pizza` and `pizzaID` are passed as the first parameter and second parameter, respectively, to the routerLink array. Thus, `pizzaID` is dynamically taken from the pizza object, pizzaObject.


<h3>2. Query parameters using router. navigate</h3>

Query parameters are those that appear after a question mark `(?)`. The parameters and their corresponding values are separated by an equal to `(=)` sign. Consider the URL `http://localhost:4200/pizzas?order=popular` to display the pizzas ordered by most users.

```ts
goPizzas(){
  this.router.navigate( ['/pizza/'], { queryParams: { order: 'popular' } } );
}
```
Query parameters are set using queryParams in Router. navigate. Multiple query parameters can be passed by passing them as comma-separated parameters along with their corresponding values.

```ts
goPizzas(){
  this.router.navigate( ['/pizza'], { queryParams: { order: 'popular', price-range: 'expensive' } } );
}
```
The resultant URL will be `http://localhost:4200/pizzas?order=popular&price-range=expensive`

<h3>3. Query parameters using queryParamsHandling</h3>

When a user navigates from one view to another, query parameters are lost. Setting queryParamsHandling to ‘preserve’ or ‘merge’ helps preserve the required query parameters.

**Note**: This feature is available only for Angular 4+.

For example, routing users from the pizzas page with the query parameter {order:’popular’} to the /billing page - while also preserving the query parameter - can be achieved in Angular with:

```ts
goToBilling() {
  this.router.navigate( [‘/billing’], { queryParamsHandling: 'preserve' } );
}
```
The resultant URL will be `http://localhost:4200/billing?order=popular`

As you can see from the URL, the user is taken to the billing page, yet the query parameter from the previous page (order=popular) is retained.

New query parameters can also be merged while still preserving the previous query parameter. Suppose we want to route users to the /billing page while also passing the query parameter {payment:’UPI’}, we can accomplish the same with the following code:

```ts
goToBilling() {
  this.router.navigate( ['/billing'], { queryParamsHandling: 'merge' } );
}
```
The resultant URL is `http://localhost:4200/billing?order=popular&payment=upi`

Note that the old parameter `(order=popular)` has been preserved while adding the new parameter `(payment=upi)`.

<h3>4. Query parameters using RouterLink</h3>

As shown in the section on URL parameters, if the routerLink directive is used for navigation, query parameters can be used along with it as follows:

```html
<a [routerLink]="['/pizzas']" [queryParams]="{ order: 'popular' }">Pizzas</a>
```

Further, ‘preserve’ or ‘merge’ can be added as another attribute to the tag by setting queryParamsHanding accordingly.

<h3>5. URL fragment</h3>

URL fragment or hash appears at the end of the URL. It is a link that jumps or, in other words, scrolls down to the content whose ID is the same as that in the fragment of the Angular router. It is also known as a named anchor and is an internal page reference.

Consider the URL `careers.com/tech#fullstackdeveloper`. It will take us to a page with details on different careers, and under tech careers, information on every specialization. The fragment (`fullstackdeveloper`) will scroll to the part of the page focusing on `fullstackdeveloper` under tech. If a user clicks on, say, `cybersecurity`, the URL will change to `careers.com/tech#cybersecurity`.

Note that the fragment changed from #fullstackdeveloper to #cybersecurity. The hash, therefore, keeps changing, depending on which tech specialization is clicked on by the visitor.

The corresponding snippet in Angular 10 is as follows:

```ts
const routes:Routes = []
const routerOptions:ExtraOptions = {
  scrollPositionRestoration:’enabled’,
  anchorScrolling:’enabled’,
};
@NgModule({
  imports:[RouterModule.forRoot(routes,routerOptions)],
  exports:[RouterModule],
})
```

We add routerOptions with the type ExtraOptions. ExtraOptions is the set of configuration options for a routing module provided in the forward method. Here, extra options can be defined. In our case, `scrollPositionRestoration` and `anchorScrolling` are the two extra options used. The `scrollPositionRestoration` option stores the scroll position and maintains it when we click on the back or forward buttons.


<h3>6. Data property</h3>

The Angular route data property helps pass static data to a route. It is an array of key-value pairs and is used to store read-only static data, such as page titles. Consider a route with a data property set as follows:

```ts
{ path: 'static', component: StaticComponent, data: { id:'1', name: "Angular" } }
```

Here, `{id:'1', name: "Mita" }` is the static data passed when the component, StaticComponent, is rendered. Observe that the key-value pairs are strings here `("Angular" and "1")` as they are enclosed within quotes.

<h3>7. RouterLink for dynamic data</h3>

Dynamic data or user-defined objects can be passed from Angular version 7.2 using the state object stored in History API. The state value can be provided using the `routerLink` directive or `navigateByURL`.

The snippet to achieve the the routerLink directive is:

```html
<a [routerLink]="['dynamic']" [state]="{ id:100 , name:'Maya'}">Dynamic Data</a>
```

<h3>8. Dynamic data using navigateByURL</h3>

An alternative method to pass dynamic data is by using navigateByURL as follows:

```ts
this.router.navigateByUrl('/dynamic', { state: { id:100 , name:'Maya' } });
```
Here, the router will add a navigationId property to the state object, so you shouldn’t use a scalar value.

<h3>9. Wildcard routes</h3>

The `double asterisk sign (**)` sets up a wildcard route in Angular. Wildcard routes are essential to handle users navigating to a path not defined in the routes. In that case, the website should route them to `Page Not Found` and so on. As it matches any given path, it should be defined as the last path.

```ts
const routes:Routes = [
  { path: 'home', component: HomeComponent },
  { path:'pizzas', component: PizzaComponent },
  { path: 'billing', component: BillingComponent },
  { path: '**', component: PageNotFoundComponent }
];
```


<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
