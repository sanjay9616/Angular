<h1>Dependency Injection in Angular</h1>

The @Injectable decorator is used to define a service in an Angular application. It indicates that the service can be injected into other components or services.

Angular's Dependency Injection is a design pattern and framework mechanism that allows you to create, manage, and inject dependencies in a component-based architecture. It promotes modular and reusable code by providing a way to declare a component's dependencies rather than having the component create or manage them.

<h2>Service</h2>

- A service is a reusable component or utility that can be injected into other components. Services are often used to encapsulate logic that multiple components can share
- Let's consider a simple example where we have a UserService that provides user-related functionality, and a UserProfileComponent that needs to use this service.

**Step 1: Create a Service**

```ts
// user.service.ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root',
})
export class UserService {
  getUser(): string {
    return 'John Doe';
  }
}
```

**Step 2: Create a Component that Injects the Service**

```ts
// user-profile.component.ts
import { Component } from '@angular/core';
import { UserService } from './user.service';

@Component({
  selector: 'app-user-profile',
  template: '<p>User Profile: {{ userProfile }}</p>',
})
export class UserProfileComponent {
  userProfile: string;

  constructor(private userService: UserService) {
    this.userProfile = this.userService.getUser();
  }
}
```

<h2>How It Works:</h2>

1. When Angular creates the UserProfileComponent, it recognizes the UserService dependency in the constructor.
2. Angular's injector identifies that UserService is provided in the root (providedIn: 'root'), so it creates a single instance of the UserService.
3. The UserProfileComponent receives the instance of UserService through dependency injection.
4. The UserProfileComponent can now use the methods and properties of UserService seamlessly.

<h2>Significance of @injectable and provideIn</h2>

- In Angular, the @Injectable decorator is used to declare a class as a service that can be injected into other components, services, or directives. 
- The providedIn option in the @Injectable decorator is used to specify the module or injector where the service should be provided. It simplifies the process of registering services by allowing you to declare the provider directly in the service file. 
- Use providedIn: 'root' for services that should be singletons and provided at the root level. This ensures that there is only one instance of the service throughout the application.

```ts
// user.service.ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root', // The service is provided at the root level (AppModule)
})
export class UserService {
  // Service logic goes here
}
```

Use providedIn: SomeModule for services that should be scoped to a specific feature module. This allows for lazy loading and ensures that each feature module gets its own instance of the service.

```ts
@Injectable({
  providedIn: MyFeatureModule,
})
export class MyFeatureService {
  // ...
}
```

<h2>Separation of Concerns Addressed By Dependency Injection:</h2>

<h3>1. Singleton Nature of Services</h3>

By default, Angular services are singletons. This means that Angular creates only one instance of a service and shares it throughout the application. When a component or another service requests a service via dependency injection, they receive the same instance of the service.

Consider our example with the UserService:

```ts
// user.service.ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root',
})
export class UserService {
  private users: string[] = ['John Doe', 'Jane Smith', 'Bob Johnson'];

  getUsers(): string[] {
    return this.users;
  }
}
```

<h3>2. Circular Dependencies</h3>

Circular dependencies occur when two or more services depend on each other directly or indirectly. Angular's Dependency Injection handles circular dependencies efficiently, ensuring that services are properly initialized without causing runtime errors. Let's explore how Angular's Dependency Injection achieves separation of concerns in the context of circular dependencies with an example.

Consider two services, UserService and ProfileService, where ProfileService depends on UserService, and UserService depends on ProfileService.

```ts
// user.service.ts
import { Injectable } from '@angular/core';
import { ProfileService } from './profile.service';

@Injectable({
  providedIn: 'root',
})
export class UserService {
  constructor(private profileService: ProfileService) {}

  getUser(): string {
    const userProfile = this.profileService.getUserProfile();
    return `User details: ${userProfile}`;
  }
}
```
```ts
// profile.service.ts
import { Injectable } from '@angular/core';
import { UserService } from './user.service';

@Injectable({
  providedIn: 'root',
})
export class ProfileService {
  constructor(private userService: UserService) {}

  getUserProfile(): string {
    const user = this.userService.getUser();
    return `${user}'s profile information`;
  }
}
```

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
