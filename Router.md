<h1>Angular Router</h1>

Angular routing is a mechanism that allows you to navigate between different components in a single-page application (SPA) without triggering a full page reload. It helps organize and structure your application by associating different views (components) with specific URLs.

**Key Terms Explained:**

1. **Route**: A route in Angular is a mapping between a URL path and a component. When a user navigates to a specific URL, the associated component is rendered.
2. **Router**: The Angular Router is a powerful module that facilitates navigation and provides a way to configure routes in your application.
3. **Router Outlet**: The <router-outlet> directive is a placeholder where the routed component will be displayed. It acts as the container for the component associated with the current route.
4. **Route Configuration**: This is where you define your application's routes. The configuration includes the path, component to be displayed, and optional data.
5. **RouterLink**: The [routerLink] directive is used in templates to create links for navigating to specific routes. It's a handy way to navigate without writing out the full URL.

Let's Break It Down...

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

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
