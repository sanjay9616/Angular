<h1>Angular Decorators</h1>

In Angular, a decorator is a function that adds metadata to a class, its members, or its method arguments. Decorators are a way to extend the functionality of a class, method, or property by attaching additional features or behaviors to them.

There are four main types that are used to provide additional information about a class or its members:

- **Class decorators**, e.g. `@Component` and `@NgModule`
- **Property decorators** for properties inside classes, e.g. `@Input` and `@Output`
- **Method decorators** for methods inside classes, e.g. `@HostListener`
- **Parameter decorators** for parameters inside class constructors, e.g. `@Injectable`

<h2>@Component</h2>

The `@Component` decorator is used to define a component in an Angular application. It takes an object with various properties, such as the component's template, style, and selector, as an argument.

```ts
import { Component, OnInit } from '@angular/core';

@Component({
    selector: 'app-pr-dashboard',
    templateUrl: './pr-dashboard.component.html',
    styleUrls: ['./pr-dashboard.component.scss']
})
export class PrDashboardComponent implements OnInit {}
```

In this example, the `@Component` decorator is applied to the PrDashboardComponent class, which defines a component with an `app-pr-dashboard` selector and a simple template.

<h2>@Input</h2>

The `@Input` decorator is used to bind a component's input property to a value that is passed from its parent component.

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent {
    @input() message: string;
}
```

In this example, the `@Input` decorator is applied to the message property of the ChildComponent class, which indicates that the message property can be bound to a value passed from the parent component.

<h2>@NgModule</h2>

- The NgModule decorator in Angular is like a blueprint for organizing and configuring different parts of your application. It’s like a set of instructions that tells Angular how to assemble the various components, directives, pipes, and services into cohesive units called modules. These modules help in managing dependencies, defining routing rules, and configuring providers.
- Essentially, the NgModule decorator serves as a central hub for defining and organizing the building blocks of an Angular application, making it easier to develop, maintain, and scale complex web applications.
- Angular NgModules are also classes with ‘@NgModule’ and it has metadata that describes how the different parts of the application will work together. Like javascript modules have their own files but NgModule does not have their own file, they only include metadata. it also helps to organize the components and services of the angular application.

```ts
import { NgModule } from '@angular/core';

@NgModule({
    declarations: [ /* Components, directives, and pipes */],
    imports: [ /* Other modules */],
    exports: [ /* Exports of this module */],
    providers: [ /* Services */],
    bootstrap: [ /* Root component */],
    entryComponents: []
})

export class MyNgModule { }
```
- Here, declarations is the array of components, directives, and pipes that belong to this module, imports is the array of other modules that this module depends on, exports is the array of declarations that should be visible and accessible to components in other modules, providers are the array of services available for injection within this module and bootstrap is the array containing the root component(s) to bootstrap when this module is loaded.
**add definition of above ngModlue keywords**

<h2>@HostListener</h2>

The `@HostListener` decorator in Angular is a function that allows you to bind a host element event to a component method. It is used to listen for events that are triggered on the host element, such as mouse events, keyboard events, and touch events.

```ts
import { HostListener, Component } from "@angular/core";

@Component({
  selector: 'app',
  template: `<h1>Hello, you have pressed enter {{counter}} number of times!</h1>
  Press enter key to increment the counter.
  <button (click)="resetCounter()">Reset Counter</button>`
})
class AppComponent {
  counter = 0;
  @HostListener('window:keydown.enter', ['$event'])
  handleKeyDown(event: KeyboardEvent) {
    this.counter++;
  }
  resetCounter() {
    this.counter = 0;
  }
}
```

The above example registers another DOM event handler that listens for Enter key-press events on the global window.

<h2>@Injectable</h2>

The @Injectable decorator is used to define a service in an Angular application. It indicates that the service can be injected into other components or services.

```ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class MyService {
    // service class goes here
}
```

In this example, the @Injectable decorator is applied to the MyService class, which defines a service that can be injected into other components or services.

<h2>Create a Custom Decorator</h2>

To create a custom decorator, you can define a function that takes the target class or its member as an argument and then adds the desired behavior or metadata. Here's an example of a custom decorator that logs a message when a method is called:

<a href="https://sagarsnath.medium.com/understanding-custom-decorators-in-angular-bbd023d141eb#:~:text=Creating%20Custom%20Decorators%3A,the%20target%20element%20being%20decorated.">IMPLEMENTATION</a>

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
