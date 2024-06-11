<h1>Route Guards in Angular</h1>

While navigating from one route to another, there are situations when we do not want an unauthenticated user to access a particular route and that is where we want to keep a check. For example, A user has subscribed to an Angular course on an online platform but he has not subscribed to any other course on the same platform, in that case, the route to the angular course page would work for him but the routes to other course modules should not be accessible by him. This is where Route Guards come into play!

So, in simple terms, we use guards to put a check to restrict the user from accessing some of the pages of our site. If the returned value by the guard is true, the user can continue navigating from one route to another, otherwise the process halts.

The return type of a route guard can be of two kinds:

- Promise <Boolean>(synchronous)
- Observable <Boolean> (asynchronous)

Route Guards are of different types, used as per their functionalities. They are:

- CanActivate
- CanActivateChild
- CanDeactivate
- Resolve
- CanLoad

<h2>CanActivate</h2>

The CanActivate guard checks whether a route can be activated. This is useful for protecting routes that should not be accessible unless certain conditions are met, like user authentication.

**Use Case: User Authentication**

Imagine you have an admin dashboard that should only be accessible to authenticated users. A CanActivate guard can check if the user is logged in before navigating to the admin page. If the user is not authenticated, the guard redirects them to a login page.

**Creating a CanActivate Guard**

To create a guard using Angular CLI, you can run: `ng generate guard auth`

```ts
import { Injectable } from '@angular/core';
import { CanActivate, Router } from '@angular/router';

@Injectable({
  providedIn: 'root'
})
export class AuthGuard implements CanActivate {

  constructor(private router: Router) {}

  canActivate(): boolean {
    if (/* your authentication condition */) {
      return true;
    } else {
      this.router.navigate(['/login']);
      return false;
    }
  }
}
```
**Adding CanActivate to Routes**
```ts
import { AuthGuard } from './auth.guard';

const routes: Routes = [
    {
        path: 'protected',
        component: ProtectedComponent,
        canActivate: [AuthGuard]
    },
  // ...
];
```

<h2>CanActivateChild</h2>

Similar to CanActivate, but it works on child routes. Useful for feature modules with multiple child routes.

**Use Case: Feature Access Control**

Suppose your application has a settings page with multiple child routes like “Profile Settings”, “Account Settings”, and “Privacy Settings”. You can use a CanActivateChild guard to ensure that only users with the appropriate permissions can access these child routes.

```ts
const childRoutes: Routes = [
    {
        path: 'child',
        component: ChildComponent,
        canActivateChild: [AuthGuard]
    },
    // ...
];
```

<h2>CanDeactivate</h2>

This guard works when you're navigating away from a component. It is often used to warn the user about unsaved changes.

**Use Case: Unsaved Changes**

You have a form page for editing profile information. If a user makes changes but tries to navigate away without saving, a CanDeactivate guard can prompt them to either save the changes or confirm that they want to leave without saving.

```ts
export interface CanComponentDeactivate {
 canDeactivate: () => boolean;
}
```
Implement this interface in your component, and you can use it in a CanDeactivate guard.

<h2>Resolve</h2>

A Resolve guard fetches data before navigation completes. The data can be used to populate route parameters.

**Use Case: Data Preloading**

In an e-commerce application, you have a product details page. A Resolve guard can pre-fetch the product details before the route is activated, ensuring that the user doesn't see an empty or partially loaded page.

```ts
@Injectable({
  providedIn: 'root'
})
export class DataResolver implements Resolve<Data> {
  resolve(route: ActivatedRouteSnapshot, state: RouterStateSnapshot): Data {
    // Fetch your data here
  }
}
```

<h2>CanLoad</h2>

CanLoad checks if a module should be lazy-loaded or not. This is important if you want to prevent unauthorized users from downloading parts of your application.

**Use Case: Feature Gating**

Your application has a premium feature module that should only be accessible (and thus downloaded) by premium users. A CanLoad guard can prevent unauthorized users from even downloading this module, saving bandwidth and enhancing security.

```ts
const routes: Routes = [
  {
    path: 'feature',
    loadChildren: () => import('./feature/feature.module').then(m => m.FeatureModule),
    canLoad: [AuthGuard]
  },
  // ...
];
```

**Registering Guards**

```ts
@NgModule({
  providers: [AuthGuard],
  // ...
})
export class AppModule {}
```

Guards in Angular provide a robust way to control navigation in your application. With various types of guards available, you can handle a variety of conditions: check user authentication, warn about unsaved changes, or even pre-fetch data before completing navigation. As a developer, understanding guards is key to ensuring both the security and data integrity of the Angular apps.

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
