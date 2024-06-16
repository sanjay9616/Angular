<h1>Angular Interview Questions and Answers</h1>

### Table of Contents

| No. | Questions                                                                                                                                               |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is Angular Framework](#What-is-Angular-Framework)                                                                                                 |
| 1   | [What is the difference between AngularJS and Angular](#What-is-the-difference-between-AngularJS-and-Angular)                                           |
| 1   | [What is TypeScript](#What-is-TypeScript)                                                                                                               |
| 1   | [Write a pictorial diagram of Angular architecture](#Write-a-pictorial-diagram-of-Angular-architecture)                                                 |
| 1   | [What are the key components of Angular](#What-are-the-key-components-of-Angular)                                                                       |
| 1   | [What are components](#What-are-components)                                                                                                             |
| 1   | [What is a template](#What-is-a-template)                                                                                                               |
| 1   | [What is Angular CLI](#What-is-Angular-CLI)                                                                                                             |
| 1   | [What is dependency injection in Angular](#What-is-dependency-injection-in-Angular)                                                                     |
| 1   | [How is Dependency Hierarchy formed](#How-is-Dependency-Hierarchy-formed)                                                                               |
| 1   | [What is the option to choose between inline and external template file](#What-is-the-option-to-choose-between-inline-and-external-template-file)       |
| 1   | [What happens if you use script tag inside template](#What-happens-if-you-use-script-tag-inside-template)                                               |
| 1   | [What are template expressions](#What-are-template-expressions)                                                                                         |
| 1   | [What are template statements](#What-are-template-statements)                                                                                           |
| 1   | [What are Angular elements](#What-are-Angular-elements)                                                                                                 |
| 1   | [What is the browser support of Angular Elements](#What-is-the-browser-support-of-Angular-Elements)                                                     |
| 1   | [What are custom elements](#What-are-custom-elements)                                                                                                   |
| 1   | [Do I need to bootstrap custom elements](#Do-I-need-to-bootstrap-custom-elements)                                                                       |
| 1   | [Explain how custom elements works internally](#Explain-how-custom-elements-works-internally)                                                           |
| 1   | [How to transfer components to custom elements](#How-to-transfer-components-to-custom-elements)                                                         |
| 1   | [What are the mapping rules between Angular component and custom element](#What-are-the-mapping-rules-between-Angular-component-and-custom-element)     |
| 1   | [How do you define typings for custom elements](#How-do-you-define-typings-for-custom-elements)                                                         |
| 1   | [What are dynamic components](#What-are-dynamic-components)                                                                                             |
| 1   | [What is Angular Universal](#What-is-Angular-Universal)                                                                                                 |
| 1   | [What is a data binding](#What-is-a-data-binding)                                                                                                       |
| 2   | [What is interpolation](#What-is-interpolation)                                                                                                         |
| 3   | [How do you categorize data binding types](#How-do-you-categorize-data-binding-types)                                                                   |
| 4   | [What is the difference between interpolated content and innerHTM](#What-is-the-difference-between-interpolated-content-and-innerHTM)                   |
| 5   | [What are lifecycle hooks available](#What-are-lifecycle-hooks-available)                                                                               |
| 6   | [What is the difference between constructor and ngOnInit](#What-is-the-difference-between-constructor-and-ngOnInit)                                     |
| 7   | [What are the lifecycle hooks of a zone](#What-are-the-lifecycle-hooks-of-a-zone)                                                                       |
| 8   | [What are directives](#What-are-directives)                                                                                                             |
| 9   | [What are the differences between Component and Directive](#What-are-the-differences-between-Component-and-Directive)                                   |
| 10  | [What is the purpose of *ngFor directive](#What-is-the-purpose-of-*ngFor-directive)                                                                     |
| 11  | [What is the purpose of *ngIf directive](#What-is-the-purpose-of-*ngIf-directive)                                                                       |
| 12  | [What are the various kinds of directives](#What-are-the-various-kinds-of-directives)                                                                   |
| 13  | [How do you create directives using CLI](#How-do-you-create-directives-using-CLI)                                                                       |
| 14  | [Give an example for attribute directives](#Give-an-example-for-attribute-directives)                                                                   |
| 15  | [What is the purpose of hidden property](#What-is-the-purpose-of-hidden-property)                                                                       |
| 16  | [What is the difference between ngIf and hidden property](#What-is-the-difference-between-ngIf-and-hidden-property)                                     |
| 17  | [What is index property in ngFor directive](#What-is-index-property-in-ngFor-directive)                                                                 |
| 18  | [What is the purpose of ngFor trackBy](#What-is-the-purpose-of-ngFor-trackBy)                                                                           |
| 19  | [What is the purpose of ngSwitch directive](#What-is-the-purpose-of-ngSwitch-directive)                                                                 |
| 20  | [How to set ngFor and ngIf on the same element](#How-to-set-ngFor-and-ngIf-on-the-same-element)                                                         |
| 4   | [What is host property in css](#What-is-host-property-in-css)                                                                                           |
| 4   | [What is metadata](#What-is-metadata)                                                                                                                   |
| 4   | [What are the restrictions of metadata](#What-are-the-restrictions-of-metadata)                                                                         |
| 4   | [What is the purpose of metadata json files](#What-is-the-purpose-of-metadata-json-files)                                                               |
| 4   | [Give an example of few metadata errors](#Give-an-example-of-few-metadata-errors)                                                                       |
| 4   | [What is metadata rewriting](#What-is-metadata-rewriting)                                                                                               |
| 4   | [What is the role of ngModule metadata in compilation process](#What-is-the-role-of-ngModule-metadata-in-compilation-process)                           |
| 4   | [What is a service](#What-is-a-service)                                                                                                                 |
| 4   | [What are class field decorators](#What-are-class-field-decorators)                                                                                     |
| 4   | [What are the class decorators in Angular](#What-are-the-class-decorators-in-Angular)                                                                   |
| 4   | [Is it possible to do aliasing for inputs and outputs](#Is-it-possible-to-do-aliasing-for-inputs-and-outputs)                                           |
| 4   | [What are pipes](#What-are-pipes)                                                                                                                       |
| 4   | [What is the purpose of async pipe](#What-is-the-purpose-of-async-pipe)                                                                                 |
| 4   | [What is a parameterized pipe](#What-is-a-parameterized-pipe)                                                                                           |
| 4   | [How do you chain pipes](#How-do-you-chain-pipes)                                                                                                       |
| 4   | [What is a custom pipe](#What-is-a-custom-pipe)                                                                                                         |
| 4   | [Give an example of custom pipe](#Give-an-example-of-custom-pipe)                                                                                       |
| 4   | [What is the difference between pure and impure pipe](#What-is-the-difference-between-pure-and-impure-pipe)                                             |
| 4   | [What is slice pipe](#What-is-slice-pipe)                                                                                                               |
| 4   | [What are the list of template expression operators](#What-are-the-list-of-template-expression-operators)                                               |
| 4   | [What is the precedence between pipe and ternary operators](#What-is-the-precedence-between-pipe-and-ternary-operators)                                 |
| 4   | [How does angular finds components, directives and pipes](#How-does-angular-finds-components,-directives-and-pipes)                                     |
| 4   | [What are Http Interceptors](#What-are-Http-Interceptors)                                                                                               |
| 4   | [What are the applications of HTTP interceptors](#What-are-the-applications-of-HTTP-interceptors)                                                       |
| 4   | [How can I use interceptor for an entire application](#How-can-I-use-interceptor-for-an-entire-application)                                             |
| 4   | [What are reactive forms](#What-are-reactive-forms)                                                                                                     |
| 4   | [What are dynamic forms](#What-are-dynamic-forms)                                                                                                       |
| 4   | [What are template driven forms](#What-are-template-driven-forms)                                                                                       |
| 4   | [What are the differences between reactive forms and template driven forms](#What-are-the-differences-between-reactive-forms-and-template-driven-forms) |
| 4   | [What are the different ways to group form controls](#What-are-the-different-ways-to-group-form-controls)                                               |
| 4   | [How do you update specific properties of a form model](#How-do-you-update-specific-properties-of-a-form-model)                                         |
| 4   | [What is the purpose of FormBuilder](#What-is-the-purpose-of-FormBuilder)                                                                               |
| 4   | [How do you verify the model changes in forms](#How-do-you-verify-the-model-changes-in-forms)                                                           |
| 4   | [What are the state CSS classes provided by ngModel](#What-are-the-state-CSS-classes-provided-by-ngModel)                                               |
| 4   | [How do you reset the form](#How-do-you-reset-the-form)                                                                                                 |
| 4   | [What are the types of validator functions](#What-are-the-types-of-validator-functions)                                                                 |
| 4   | [Can you give an example of built-in validators](#Can-you-give-an-example-of-built-in-validators)                                                       |
| 4   | [How do you optimize the performance of async validators](#How-do-you-optimize-the-performance-of-async-validators)                                     |
| 4   | [What is Angular Router](#What-is-Angular-Router)                                                                                                       |
| 4   | [What is the purpose of base href tag](#What-is-the-purpose-of-base-href-tag)                                                                           |
| 4   | [What are the router imports](#What-are-the-router-imports)                                                                                             |
| 4   | [What is router outlet](#What-is-router-outlet)                                                                                                         |
| 4   | [What are router links](#What-are-router-links)                                                                                                         |
| 4   | [What are active router links](#What-are-active-router-links)                                                                                           |
| 4   | [What is router state](#What-is-router-state)                                                                                                           |
| 4   | [What are router events](#What-are-router-events)                                                                                                       |
| 4   | [What is activated route](#What-is-activated-route)                                                                                                     |
| 4   | [How do you define routes](#How-do-you-define-routes)                                                                                                   |
| 4   | [What is the purpose of Wildcard route](#What-is-the-purpose-of-Wildcard-route)                                                                         |
| 4   | [Do I need a Routing Module always](#Do-I-need-a-Routing-Module-always)                                                                                 |
| 4   | [How do you detect route change in Angular](#How-do-you-detect-route-change-in-Angular)                                                                 |
| 4   | [How can I use SASS in angular project](#How-can-I-use-SASS-in-angular-project)                                                                         |
| 4   | [How do you get the current route](#How-do-you-get-the-current-route)                                                                                   |
| 4   | [Is Angular supports dynamic imports](#Is-Angular-supports-dynamic-imports)                                                                             |
| 4   | [What is lazy loading](#What-is-lazy-loading)                                                                                                           |
| 4   | [What are different types of compilation in Angular](#What-are-different-types-of-compilation-in-Angular)                                               |
| 4   | [What is JIT](#What-is-JIT)                                                                                                                             |
| 4   | [What is AOT](#What-is-AOT)                                                                                                                             |
| 4   | [What is AOT compiler](#What-is-AOT-compiler)                                                                                                           |
| 4   | [Why do we need compilation process](#Why-do-we-need-compilation-process)                                                                               |
| 4   | [What are the advantages with AOT](#What-are-the-advantages-with-AOT)                                                                                   |
| 4   | [What are the ways to control AOT compilation](#What-are-the-ways-to-control-AOT-compilation)                                                           |
| 4   | [What are the three phases of AOT](#What-are-the-three-phases-of-AOT)                                                                                   |
| 4   | [Can I use arrow functions in AOT](#Can-I-use-arrow-functions-in-AOT)                                                                                   |
| 4   | [Can I use any javascript feature for expression syntax in AOT](#Can-I-use-any-javascript-feature-for-expression-syntax-in-AOT)                         |

### <h2>What is Angular Framework</h2>

Angular is a **TypeScript-based open-source** front-end platform that makes it easy to build web, mobile and desktop applications. The major features of this framework include declarative templates, dependency injection, end to end tooling which ease application development.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the difference between AngularJS and Angular</h2>

Angular is a completely revived component-based framework in which an application is a tree of individual components.

Here are some of the major differences in tabular format:-

| AngularJS                                   | Angular                                  |
| ------------------------------------------- | ---------------------------------------- |
| It is based on MVC architecture             | This is based on Service/Controller      |
| It uses JavaScript to build the application | Uses TypeScript to build the application |
| Based on controllers concept                | This is a component based UI approach    |
| No support for mobile platforms             | Fully supports mobile platforms          |
| Difficult to build SEO friendly application | Ease to build SEO friendly applications  |

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is TypeScript</h2>

TypeScript is a strongly typed superset of JavaScript created by Microsoft that adds optional types, classes, async/await and many other features, and compiles to plain JavaScript. Angular is written entirely in TypeScript as a primary language.

You can install TypeScript globally as

```cmd
npm install -g typescript
```

Let's see a simple example of TypeScript usage:-

```typescript
function greeter(person: string) {
    return "Hello, " + person;
}

let user = "Sudheer";

document.body.innerHTML = greeter(user);
```

The greeter method allows only string type as argument.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Write a pictorial diagram of Angular architecture</h2>

The main building blocks of an Angular application are shown in the diagram below:-

<img src="https://v2.angular.io/resources/images/devguide/architecture/overview2.png">

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the key components of Angular</h2>

Angular has the key components below,

1. **Component:** These are the basic building blocks of an Angular application to control HTML views.
2. **Modules:** An Angular module is a set of angular basic building blocks like components, directives, services etc. An application is divided into logical pieces and each piece of code is called as "module" which perform a single task.
3. **Templates:** These represent the views of an Angular application.
4. **Services:** Are used to create components which can be shared across the entire application.
5. **Metadata:** This can be used to add more data to an Angular class.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are components</h2>

Components are the most basic UI building block of an Angular app, which form a tree of Angular components. These components are a subset of directives. Unlike directives, components always have a template, and only one component can be instantiated per element in a template.

Let's see a simple example of Angular component

```typescript
import { Component } from '@angular/core';

@Component ({
    selector: 'my-app',
    template: ` <div>
        <h1>{{title}}</h1>
        <div>Learn Angular6 with examples</div>
    </div> `,
})

export class AppComponent {
    title: string = 'Welcome to Angular world';
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a template</h2>

A template is a HTML view where you can display data by binding controls to properties of an Angular component. You can store your component's template in one of two places. You can define it inline using the template property, or you can define the template in a separate HTML file and link to it in the component metadata using the @Component decorator's templateUrl property.

**Using inline template with template syntax,**

```typescript
import { Component } from '@angular/core';

@Component ({
    selector: 'my-app',
    template: '
        <div>
            <h1>{{title}}</h1>
            <div>Learn Angular</div>
        </div>
    '
})

export class AppComponent {
    title: string = 'Hello World';
}
```

**Using separate template file such as app.component.html**

```typescript
import { Component } from '@angular/core';

@Component ({
    selector: 'my-app',
    templateUrl: 'app/app.component.html'
})

export class AppComponent {
    title: string = 'Hello World';
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is Angular CLI</h2>

Angular CLI(**Command Line Interface**) is a command line interface to scaffold and build angular apps using nodejs style (commonJs) modules.

You need to install using below npm command,

```
npm install @angular/cli@latest
```

Below are the list of few commands, which will come handy while creating angular projects

1. **Creating New Project:** ng new <project-name>

2. **Generating Components, Directives & Services:** ng generate/g <feature-name>

The different types of commands would be,

- ng generate class my-new-class: add a class to your application
- ng generate component my-new-component: add a component to your application
- ng generate directive my-new-directive: add a directive to your application
- ng generate enum my-new-enum: add an enum to your application
- ng generate module my-new-module: add a module to your application
- ng generate pipe my-new-pipe: add a pipe to your application
- ng generate service my-new-service: add a service to your application

3. **Running the Project:** ng serve

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is dependency injection in Angular</h2>

Dependency injection (DI), is an important application design pattern in which a class asks for dependencies from external sources rather than creating them itself. Angular comes with its own dependency injection framework for resolving dependencies( services or objects that a class needs to perform its function).So you can have your services depend on other services throughout your application.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How is Dependency Hierarchy formed</h2>

Injectors in Angular have rules that can be leveraged to achieve the desired visibility of injectables in your applications. By understanding these rules, you can determine in which NgModule, Component, or Directive you should declare a provider.

**1. Angular has two injector hierarchies:**

| Injecter Hierarchies        | Details                                                                                                                                     |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `ModuleInjector` Hierarchy  | Configure a ModuleInjector in this hoerarchy using an @NgModule or @Injectable annotation.                                                  |
| `ElementInjector` Hierarchy | Created a implicitly at each DOM element. An ElementInjector is empty by default it in the providers property on @Directive or @Component() |

**2. Module injector**

When angular starts, it creates a root injector where the services will be registered, these are provided via injectable annotation. All services provided in the `ng-model` property are called providers (if those modules are not lazy-loaded).

Angular recursively goes through all models which are being used in the application and creates instances for provided services in the root injector. If you provide some service in an eagerly-loaded model, the service will be added to the root injector, which makes it available across the whole application.

**3. Platform Module**

During application bootstrapping angular creates a few more injectors, above the root injector goes the platform injector, this one is created by the platform browser dynamic function inside the `main.ts` file, and it provides some platform-specific features like `DomSanitizer`. 

**4. NullInjector()**

At the very top, the next parent injector in the hierarchy is the `NullInjector()`.The responsibility of this injector is to throw the error if something tries to find dependencies there, unless you've used `@Optional()` because ultimately, everything ends at the `NullInjector()` and it returns an error or, in the case of `@Optional()`, `null`.

<img src="https://media.licdn.com/dms/image/D5622AQG87_LQY3-BTw/feedshare-shrink_800/0/1690728701291?e=1721260800&v=beta&t=Z_gCyPlio-_yIbLJ15fCThe8IQmrxLquKxHWfhf7Eh0">


**5. ElementInjector**

Angular creates `ElementInjector` hierarchies implicitly for each DOM element. `ElementInjector` injector is being created for any tag that matches the angular component, or any tag on which directive is applied, and you can configure it in component and directive annotations inside the provider's property, thus, it creates its own hierarchy likewise the upper one.

<img src="https://github.com/sanjay9616/Angular/assets/87460579/8bfb714d-d709-4b56-890d-c49b94c301ad">


**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the option to choose between inline and external template file</h2>

You can store your component's template in one of two places. You can define it inline using the **template** property, or you can define the template in a separate HTML file and link to it in the component metadata using the **@Component** decorator's **templateUrl** property.

The choice between inline and separate HTML is a matter of taste, circumstances, and organization policy. But normally we use inline template for small portion of code and external template file for bigger views. By default, the Angular CLI generates components with a template file. But you can override that with the below command,
```
ng generate component hero -it
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What happens if you use script tag inside template</h2>

Angular recognizes the value as unsafe and automatically sanitizes it, which removes the `script` tag but keeps safe content such as the text content of the `script` tag. This way it eliminates the risk of script injection attacks. If you still use it then it will be ignored and a warning appears in the browser console.

Let's take an example of innerHtml property binding which causes XSS vulnerability,

```typescript
export class InnerHtmlBindingComponent {
    // For example, a user/attacker-controlled value from a URL.
    htmlSnippet = 'Template <script>alert("0wned")</script> <b>Syntax</b>';
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are template expressions</h2>

A template expression produces a value similar to any Javascript expression. Angular executes the expression and assigns it to a property of a binding target; the target might be an HTML element, a component, or a directive. In the property binding, a template expression appears in quotes to the right of the = symbol as in `[property]="expression"`.

In interpolation syntax, the template expression is surrounded by double curly braces. For example, in the below interpolation, the template expression is `{{username}}`,

```html
<h3>{{username}}, welcome to Angular</h3>
```

The below javascript expressions are prohibited in template expression
1. assignments (=, +=, -=, ...)
2. new
3. chaining expressions with ; or ,
4. increment and decrement operators (++ and --)


**[⬆ Back to Top](#table-of-contents)**

### <h2>What are template statements</h2>

 A template statement responds to an event raised by a binding target such as an element, component, or directive. The template statements appear in quotes to the right of the = symbol like `(event)="statement"`.

Let's take an example of button click event's statement

```html
<button (click)="editProfile()">Edit Profile</button>
```

In the above expression, editProfile is a template statement. The below JavaScript syntax expressions are not allowed.

1. new
2. increment and decrement operators, ++ and --
3. operator assignment, such as += and -=
4. the bitwise operators | and &
5. the template expression operators


**[⬆ Back to Top](#table-of-contents)**

### <h2>What are Angular elements</h2>

Angular elements are Angular components packaged as **custom elements** (a web standard for defining new HTML elements in a framework-agnostic way). Angular Elements host an Angular component, providing a bridge between the data and the logic defined in the component and the standard DOM APIs, thus, providing a way to use Angular components in `non-Angular environments`.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the browser support of Angular Elements</h2>

Since Angular elements are packaged as custom elements the browser support of angular elements is same as custom elements support.

This feature is is currently supported natively in a number of browsers and pending for other browsers.

| Browser | Angular Element Support                                                                                                                                 |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Chrome  | Natively supported                                                                                                                                      |
| Opera   | Natively supported                                                                                                                                      |
| Safari  | Natively supported                                                                                                                                      |
| Firefox | Natively supported from 63 version onwards. You need to enable dom.webcomponents.enabled and dom.webcomponents.customelements.enabled in older browsers |
| Edge    | Currently it is in progress                                                                                                                             |

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are custom elements</h2>

Custom elements (or Web Components) are a Web Platform feature which extends HTML by allowing you to define a tag whose content is created and controlled by JavaScript code. The browser maintains a `CustomElementRegistry` of defined custom elements, which maps an instantiable JavaScript class to an HTML tag. Currently this feature is supported by Chrome, Firefox, Opera, and Safari, and available in other browsers through polyfills.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Do I need to bootstrap custom elements</h2>

No, custom elements bootstrap (or start) automatically when they are added to the DOM, and are automatically destroyed when removed from the DOM. Once a custom element is added to the DOM for any page, it looks and behaves like any other HTML element, and does not require any special knowledge of Angular.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Explain how custom elements works internally</h2>

Below are the steps in an order about custom elements functionality,

1. **App registers custom element with browser:** Use the `createCustomElement()` function to convert a component into a class that can be registered with the browser as a custom element.
2. **App adds custom element to DOM:**  Add custom element just like a built-in HTML element directly into the DOM.
3. **Browser instantiate component based class:** Browser creates an instance of the registered class and adds it to the DOM.
4. **Instance provides content with data binding and change detection:** The content with in template is rendered using the component and DOM data.

The flow chart of the custom elements functionality would be as follows,

**[⬆ Back to Top](#table-of-contents)**

### <h2>How to transfer components to custom elements</h2>

Transforming components to custom elements involves **two** major steps,

1. **Build custom element class:** Angular provides the `createCustomElement()` function for converting an Angular component (along with its dependencies) to a custom element. The conversion process implements `NgElementConstructor` interface, and creates a constructor class which is used to produce a self-bootstrapping instance of Angular component.
2. **Register element class with browser:** It uses `customElements.define()` JS function, to register the configured constructor and its associated custom-element tag with the browser's `CustomElementRegistry`. When the browser encounters the tag for the registered element, it uses the constructor to create a custom-element instance.

The detailed structure would be as follows,


**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the mapping rules between Angular component and custom element</h2>

The Component properties and logic maps directly into HTML attributes and the browser's event system. Let us describe them in two steps,

1. The createCustomElement() API parses the component input properties with corresponding attributes for the custom element. For example, component @Input('myInputProp') converted as custom element attribute `my-input-prop`.
2. The Component outputs are dispatched as HTML Custom Events, with the name of the custom event matching the output name. For example, component @Output() valueChanged = new EventEmitter() converted as custom element with dispatch event as "valueChanged".

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you define typings for custom elements</h2>

You can use the `NgElement` and `WithProperties` types exported from @angular/elements.

Let's see how it can be applied by comparing with Angular component.

1. The simple container with input property would be as below,

```javascript
@Component(...)
class MyContainer {
    @Input() message: string;
}
```

2. After applying types typescript validates input value and their types,

```javascirpt
const container = document.createElement('my-container') as NgElement & WithProperties<{message: string}>;
container.message = 'Welcome to Angular elements!';
container.message = true;  // <-- ERROR: TypeScript knows this should be a string.
container.greet = 'News';  // <-- ERROR: TypeScript knows there is no `greet` property on `container`.
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are dynamic components</h2>

Dynamic components are the components in which the component's location in the application is not defined at build time i.e. they are not used in any angular template. Instead, the component is instantiated and placed in the application at runtime.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is Angular Universal</h2>

Angular Universal is a server-side rendering module for Angular applications in various scenarios. This is a community driven project and available under @angular/platform-server package. Recently Angular Universal is integrated with Angular CLI.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a data binding</h2>

Data binding is a core concept in Angular and allows to define communication between a component and the DOM, making it very easy to define interactive applications without worrying about pushing and pulling data. There are four forms of data binding(divided as 3 categories) which differ in the way the data is flowing.

<h3>1. From the Component to the DOM:</h3>

- **Interpolation**: {{ value }}: Adds the value of a property from the component

```html
<li>Name: {{ user.name }}</li>
<li>Address: {{ user.address }}</li>
```

- **Property binding**: [property]=”value”: The value is passed from the component to the specified property or simple HTML attribute

```html
<input type="email" [value]="user.email">
```

<h3>2. From the DOM to the Component:</h3>

- happens (eg.: click, change, keyup), call the specified method in the component

```html
<button (click)="logout()"></button>
```

<h3>3. From the DOM to the Component:</h3>

- data flow both ways. For example, in the below code snippet, both the email DOM input and component email property are in sync

```html
<input type="email" [(ngModel)]="user.email">
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is interpolation</h2>

Interpolation is a special syntax that Angular converts into property binding. It’s a convenient alternative to property binding. It is represented by double curly braces({{}}). The text between the braces is often the name of a component property. Angular replaces that name with the string value of the corresponding component property.

Let's take an example,

```html
<h3>
  {{title}}
  <img src="{{url}}" style="height:30px">
</h3>
```

In the example above, Angular evaluates the title and url properties and fills in the blanks, first displaying a bold application title and then a URL.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you categorize data binding types</h2>

Binding types can be grouped into three categories distinguished by the direction of data flow. They are listed as below,

1. From the source-to-view
2. From view-to-source
3. View-to-source-to-view

The possible binding syntax can be tabularized as below,

| Data direction                   | Syntax                                                                 | Type                                             |
| -------------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------ |
| From the source-to-view(One-way) | 1. {{expression}} 2. [target]="expression" 3. bind-target="expression" | Interpolation, Property, Attribute, Class, Style |
| From view-to-source(One-way)     | 1. (target)="statement" 2. on-target="statement"                       | Event                                            |
| View-to-source-to-view(Two-way)  | 1. [(target)]="expression" 2. bindon-target="expression"               | Two-way                                          |

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the difference between interpolated content and innerHTM</h2>

The main difference between interpolated and innerHTML code is the behavior of code interpreted. Interpolated content is always escaped i.e,  HTML isn't interpreted and the browser displays angle brackets in the element's text content. Where as in innerHTML binding, the content is interpreted i.e, the browser will convert < and > characters as HTMLEntities. For example, the usage in template would be as below,

```html
<p>Interpolated value:</p>
<div >{{htmlSnippet}}</div>
<p>Binding of innerHTML:</p>
<div [innerHTML]="htmlSnippet"></div>
```

and the property defined in a component.

```javascript
export class InnerHtmlBindingComponent {
    htmlSnippet = 'Template <script>alert("XSS Attack")</script> <b>Code attached</b>';
}
```

Even though innerHTML binding create a chance of XSS attack, Angular recognizes the value as unsafe and automatically sanitizes it.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are lifecycle hooks available</h2>

Angular application goes through an entire set of processes or has a lifecycle right from its initiation to the end of the application.The representation of lifecycle in pictorial representation as follows,

<img src="https://media.licdn.com/dms/image/C5612AQHH-keKNUYirw/article-inline_image-shrink_1500_2232/0/1648102509784?e=1723075200&v=beta&t=PwfmG35SAngielKeuHWn641XwJOFkx7aGzZTwNiwT30" alt="not found">

The description of each lifecycle method is as below,

1. **ngOnChanges:** When the value of a data bound property changes, then this method is called.
2. **ngOnInit:** This is called whenever the initialization of the directive/component after Angular first displays the data-bound properties happens.
3. **ngDoCheck:** This is for the detection and to act on changes that Angular can't or won't detect on its own.
4. **ngAfterContentInit:** This is called in response after Angular projects external content into the component's view.
5. **ngAfterContentChecked:** This is called in response after Angular checks the content projected into the component.
6. **ngAfterViewInit:** This is called in response after Angular initializes the component's views and child views.
7. **ngAfterViewChecked:** This is called in response after Angular checks the component's views and child views.
8. **ngOnDestroy:** This is the cleanup phase just before Angular destroys the directive/component.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the difference between constructor and ngOnInit</h2>

The **Constructor** is a default method of the class that is executed when the class is instantiated and ensures proper initialisation of fields in the class and its subclasses. Angular, or better Dependency Injector (DI), analyses the constructor parameters and when it creates a new instance by calling new MyClass() it tries to find providers that match the types of the constructor parameters, resolves them and passes them to the constructor. **ngOnInit** is a life cycle hook called by Angular to indicate that Angular is done creating the component. Mostly we use ngOnInit for all the initialization/declaration and avoid stuff to work in the constructor. The constructor should only be used to initialize class members but shouldn't do actual "work". So you should use constructor() to setup Dependency Injection and not much else. ngOnInit() is better place to "start" - it's where/when components' bindings are resolved.

```typescript
export class App implements OnInit {
    constructor(private myService: MyService){
        //called first time before the ngOnInit()
    }

    ngOnInit() {
        //called after the constructor and called  after the first ngOnChanges()
        //e.g. http call...
    }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the lifecycle hooks of a zone</h2>

There are four lifecycle hooks for asynchronous operations from zone.js.

1. **onScheduleTask:** This hook triggers when a new asynchronous task is scheduled. For example, when you call setTimeout()

```js
onScheduleTask: function(delegate, curr, target, task) {
    console.log('new task is scheduled:', task.type, task.source);
    return delegate.scheduleTask(target, task);
}
```

2. **onInvokeTask:** This hook triggers when an asynchronous task is about to execute. For example, when the callback of setTimeout() is about to execute.

```js
onInvokeTask: function(delegate, curr, target, task, applyThis, applyArgs) {
    console.log('task will be invoked:', task.type, task.source);
    return delegate.invokeTask(target, task, applyThis, applyArgs);
}
```

3. **onHasTask:** This hook triggers when the status of one kind of task inside a zone changes from stable(no tasks in the zone) to unstable(a new task is scheduled in the zone) or from unstable to stable.

```js
onHasTask: function(delegate, curr, target, hasTaskState) {
    console.log('task state changed in the zone:', hasTaskState);
    return delegate.hasTask(target, hasTaskState);
}
```

1. **onInvoke:** This hook triggers when a synchronous function is going to execute in the zone.

```js
onInvoke: function(delegate, curr, target, callback, applyThis, applyArgs) {
    console.log('the callback will be invoked:', callback);
    return delegate.invoke(target, callback, applyThis, applyArgs);
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are directives</h2>

Directives add behaviour to an existing DOM element or an existing component instance.

```typescript
import { Directive, ElementRef, Input } from '@angular/core';

@Directive({ selector: '[myHighlight]' })
export class HighlightDirective {
    constructor(el: ElementRef) {
        el.nativeElement.style.backgroundColor = 'yellow';
    }
}
```

Now this directive extends HTML element behavior with a yellow background as below

```html
<p myHighlight>Highlight me!</p>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the differences between Component and Directive</h2>

In a short note, A component(@component) is a directive-with-a-template.

Some of the major differences are mentioned in a tabular form

| Component                                                               | Directive                                                      |
| ----------------------------------------------------------------------- | -------------------------------------------------------------- |
| To register a component we use @Component meta-data annotation          | To register a directive we use @Directive meta-data annotation |
| Components are typically used to create UI widgets                      | Directives are used to add behavior to an existing DOM element |
| Component is used to break down the application into smaller components | Directive is used to design re-usable components               |
| Only one component can be present per DOM element                       | Many directives can be used per DOM element                    |
| @View decorator or templateurl/template are mandatory                   | Directive doesn't use View                                     |

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of *ngFor directive</h2>

We use Angular `*ngFor` directive in the template to display each item in the list. For example, here we can iterate over a list of users:

```html
<li *ngFor="let user of users">
    {{ user }}
</li>
```
The user variable in the `*ngFor` double-quoted instruction is a **template input variable**.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of *ngIf directive</h2>

Sometimes an app needs to display a view or a portion of a view only under specific circumstances. The Angular `*ngIf` directive inserts or removes an element based on a truthy/falsy condition. Let's take an example to display a message if the user age is more than 18:

```html
<p *ngIf="user.age > 18">You are not eligible for student pass!</p>
```
**Note:** Angular isn't showing and hiding the message. It is adding and removing the paragraph element from the DOM. That improves performance, especially in the larger projects with many data bindings.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the various kinds of directives</h3>

There are mainly three kinds of directives:

1. **Components** — These are directives with a template.

```typescript
import { Directive } from '@angular/core';
@Directive({
    selector: '[changeUser]'
})

export class ChangeUserDirective {
    constructor() { }
}
```
1. **Structural directives** — These directives change the DOM **layout** by adding and removing DOM elements, ex - *ngIf, *ngFor, *ngSwitch.
2. **Attribute directives** — These directives change the appearance or behavior of an element, component, or another directive, ex - ngClass, ngStyle, ngModel.

**Syntax for ngClass**

`[ngClass]="{'class': true}"`, `[ngClass]="[condiion ? 'class1' : 'class2']"`, `[ngClass]="{'class1': true, 'class2': true, 'class3': true}"`

**Syntax for ngStyle**

`[ngStyle]="{'background-color':'green'}"`, `[ngStyle]="{'background-color': condition ? 'green' : ‘red’}"`

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you create directives using CLI</h2>

You can use CLI command `ng generate directive` to create the directive class file. It creates the source file(`src/app/components/directivename.directive.ts`), the respective test file `.spec.ts` and declare the directive class file in root module.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Give an example for attribute directives</h2>

Let's take simple highlighter behavior as a example directive for DOM element. You can create and apply the attribute directive using below step:

1. Create HighlightDirective class with the file name `src/app/highlight.directive.ts`. In this file, we need to import **Directive** from core library to apply the metadata and **ElementRef** in the directive's constructor to inject a reference to the host DOM element ,

```javascript
import { Directive, ElementRef } from '@angular/core';

@Directive({
    selector: '[appHighlight]'
})
export class HighlightDirective {
    constructor(el: ElementRef) {
        el.nativeElement.style.backgroundColor = 'red';
    }
}
```
2. Apply the attribute directive as an attribute to the host element(for example, <p>)

```javascript
<p appHighlight>Highlight me!</p>
```

3. Run the application to see the highlight behavior on paragraph element

```javascript
ng serve
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of hidden property</h2>

The hidden property is used  to show or hide the associated DOM element, based on an expression. It can be compared close to `ng-show` directive in AngularJS. Let's say you want to show user name based on the availability of user using `hidden` property.

```html
<div [hidden]="!user.name">
    My name is: {{user.name}}
</div>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the difference between ngIf and hidden property</h2>

The main difference is that *ngIf will remove the element from the DOM, while [hidden] actually plays with the CSS style by setting `display:none`. Generally it is expensive to add and remove stuff from the DOM for frequent actions.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is index property in ngFor directive</h2>

The index property of the NgFor directive is used to return the zero-based index of the item in each iteration. You can capture the index in a template input variable and use it in the template.

For example, you can capture the index in a variable named indexVar and displays it with the todo's name using ngFor directive as below.

```html
<div *ngFor="let todo of todos; let i=index">{{i + 1}} - {{todo.name}}</div>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of ngFor trackBy</h2>

The main purpose of using *ngFor with trackBy option is performance optimization. Normally if you use NgFor with large data sets, a small change to one item by removing or adding an item, can trigger a cascade of DOM manipulations. In this case, Angular sees only a fresh list of new object references and to replace the old DOM elements with all new DOM elements. You can help Angular to track which items added or removed by providing a `trackBy` function which takes the index and the current item as arguments and needs to return the unique identifier for this item.

For example, lets set trackBy to the trackByTodos() method
```html
<div *ngFor="let todo of todos; trackBy: trackByTodos">
    ({{todo.id}}) {{todo.name}}
</div>
```
and define the trackByTodos method,

```javascript
trackByTodos(index: number, item: Todo): number { return todo.id; }
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of ngSwitch directive</h2>

**NgSwitch** directive is similar to JavaScript switch statement which displays one element from among several possible elements, based on a switch condition. In this case only the selected element placed into the DOM. It has been used along with `NgSwitch`, `NgSwitchCase` and `NgSwitchDefault` directives.

For example, let's display the browser details based on selected browser using ngSwitch directive.
```html
<div [ngSwitch]="currentBrowser.name">
    <chrome-browser *ngSwitchCase="'chrome'" [item]="currentBrowser"></chrome-browser>
    <firefox-browser *ngSwitchCase="'firefox'" [item]="currentBrowser"></firefox-browser>
    <opera-browser *ngSwitchCase="'opera'" [item]="currentBrowser"></opera-browser>
    <safari-browser *ngSwitchCase="'safari'" [item]="currentBrowser"></safari-browser>
    <ie-browser *ngSwitchDefault [item]="currentItem"></ie-browser>
</div>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How to set ngFor and ngIf on the same element</h2>

Sometimes you may need to both ngFor and ngIf on the same element but unfortunately you are going to encounter below template error.

```cmd
Template parse errors: Can't have multiple template bindings on one element.
```
In this case, You need to use either ng-container or ng-template.

Let's say if you try to loop over the items only when the items are available, the below code throws an error in the browser

```html
<ul *ngIf="items" *ngFor="let item of items">
    <li></li>
</ul>
```
and it can be fixed by

```html
<ng-container *ngIf="items">
    <ul *ngFor="let item of items">
        <li></li>
    </ul>
</ng-container>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is host property in css</h2>

The `:host` pseudo-class selector is used to target styles in the element that hosts the component. Since the host element is in a parent component's template, you can't reach the host element from inside the component by other means.

For example, you can create a border for parent element as below,

```js
//Other styles for app.component.css
//...
:host {
    display: block;
    border: 1px solid black;
    padding: 20px;
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is metadata</h2>

Metadata is used to decorate a class so that it can configure the expected behavior of the class. The metadata is represented by decorators

1. **Class decorators**, e.g. `@Component` and `@NgModule`

```typescript
import { NgModule, Component } from '@angular/core';

@Component({
    selector: 'my-component',
    template: '<div>Class decorator</div>',
})
export class MyComponent {
    constructor() {
        console.log('Hey I am a component!');
    }
}

@NgModule({
    imports: [],
    declarations: [],
})
export class MyModule {
    constructor() {
        console.log('Hey I am a module!');
    }
}
```
2. **Property decorators** Used for properties inside classes, e.g. `@Input` and `@Output`

```typescript
import { Component, Input } from '@angular/core';

@Component({
    selector: 'my-component',
    template: '<div>Property decorator</div>'
})

export class MyComponent {
    @Input()
    title: string;
}
```
3. **Method decorators** Used for methods inside classes, e.g. `@HostListene`r

```typescript
import { Component, HostListener } from '@angular/core';

@Component({
    selector: 'my-component',
    template: '<div>Method decorator</div>'
})

export class MyComponent {
    @HostListener('click', ['$event'])
    onHostClick(event: Event) {
    // clicked, `event` available
    }
}
```
4. **Parameter decorators** Used for parameters inside class constructors, e.g. `@Inject`, `@Optional`

```typescript
import { Component, Inject } from '@angular/core';
import { MyService } from './my-service';

@Component({
    selector: 'my-component',
    template: '<div>Parameter decorator</div>'
})
export class MyComponent {
    constructor(@Inject(MyService) myService) {
        console.log(myService); // MyService
    }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the restrictions of metadata</h2>

In Angular, You must write metadata with the following general constraints,

1. Write expression syntax with in the supported range of javascript features
2. The compiler can only reference symbols which are exported
3. Only call the functions supported by the compiler
4. Decorated and data-bound class members must be public.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of metadata json files</h2>

The metadata.json file can be treated as a diagram of the overall structure of a decorator's metadata, represented as an abstract syntax tree(AST). During the analysis phase, the AOT collector scan the metadata recorded in the Angular decorators and outputs metadata information in .metadata.json files, one per .d.ts file.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Give an example of few metadata errors</h2>

Below are some of the errors encountered in metadata,

1. **Expression form not supported:** Some of the language features outside of the compiler's restricted expression syntax used in angular metadata can produce this error.
Let's see some of these examples,

```javascript
1. export class User { ... }
    const prop = typeof User; // typeof is not valid in metadata
2. { provide: 'token', useValue: { [prop]: 'value' } }; // bracket notation is not valid in metadata
```

2. **Reference to a local (non-exported) symbol:** The compiler encountered a referenced to a locally defined symbol that either wasn't exported or wasn't initialized.
Let's take example of this error,

```javascript
// ERROR
let username: string; // neither exported nor initialized

@Component({
    selector: 'my-component',
    template: ... ,
    providers: [
        { provide: User, useValue: username }
    ]
})
export class MyComponent {}
```

You can fix this by either exporting or initializing the value,

```javascript
export let username: string; // exported
(or)
let username = 'John'; // initialized
```

3. **Function calls are not supported:** The compiler does not currently support function expressions or lambda functions. For example, you cannot set a provider's useFactory to an anonymous function or arrow function as below.

```javascript
providers: [
    { provide: MyStrategy, useFactory: function() { ... } },
    { provide: OtherStrategy, useFactory: () => { ... } }
]
```

You can fix this with exported function

```javascript
export function myStrategy() { ... }
export function otherStrategy() { ... }
... // metadata
providers: [
    { provide: MyStrategy, useFactory: myStrategy },
    { provide: OtherStrategy, useFactory: otherStrategy },
```
4. **Destructured variable or constant not supported:** The compiler does not support references to variables assigned by destructuring.
For example, you cannot write something like this:

```javascript
import { user } from './user';

// destructured assignment to name and age
const {name, age} = user;
... //metadata
providers: [
    {provide: Name, useValue: name},
    {provide: Age, useValue: age},
]
```

You can fix this by non-destructured values

```ts
import { user } from './user';
... //metadata
providers: [
    {provide: Name, useValue: user.name},
    {provide: Age, useValue: user.age},
]
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is metadata rewriting</h2>

Metadata rewriting is the process in which the compiler converts the expression initializing the fields such as useClass, useValue, useFactory, and data into an exported variable, which replaces the expression. Remember that the compiler does this rewriting during the emit of the .js file but not in definition files( .d.ts file).

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the role of ngModule metadata in compilation process</h2>

The `@NgModule` metadata is used to tell the Angular compiler what components to be compiled for this module and how to link this module with other modules.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a service</h2>

A service is used when a common functionality needs to be provided to various modules. Services allow for greater separation of concerns for your application and better modularity by allowing you to extract common functionality out of components.

Let's create a repoService which can be used across components,

```typescript
import { Injectable } from '@angular/core';
import { Http } from '@angular/http';

@Injectable({ // The Injectable decorator is required for dependency injection to work
    // providedIn option registers the service with a specific NgModule
    providedIn: 'root',  // This declares the service with the root app (AppModule)
})
export class RepoService{
    constructor(private http: Http){
    }

    fetchAll(){
    return this.http.get('https://api.github.com/repositories');
    }
}
```
The above service uses Http service as a dependency.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are class field decorators</h2>

The class field decorators are the statements declared immediately before a field in a class definition that defines the type of that field. Some of the examples are: @input and @output,

```javascript
@Input() myProperty;
@Output() myEvent = new EventEmitter();
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the class decorators in Angular</h2>

A class decorator is a decorator that appears immediately before a class definition, which declares the class to be of the given type, and provides metadata suitable to the type

The following list of decorators comes under class decorators,

1. @Component()
2. @Directive()
3. @Pipe()
4. @Injectable()
5. @NgModule()

**[⬆ Back to Top](#table-of-contents)**

### <h2>Is it possible to do aliasing for inputs and outputs</h2>

Yes, it is possible to do aliasing for inputs and outputs in two ways.

1. **Aliasing in metadata:** The inputs and outputs in the metadata aliased using a colon-delimited (:) string with the directive property name on the left and the public alias on the right. i.e. It will be in the format of propertyName:alias.

```ts
    inputs: ['input1: buyItem'],
    outputs: ['outputEvent1: completedEvent']
```
2. **Aliasing with @Input()/@Output() decorator:** The alias can be specified for the property name by passing the alias name to the @Input()/@Output() decorator.i.e. It will be in the form of @Input(alias) or @Output(alias).

```ts
    @Input('buyItem') input1: string;
    @Output('completedEvent') outputEvent1 = new EventEmitter<string>();
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are pipes</h2>

Pipes are simple functions that use [template expressions](#what-are-template-expressions) to accept data as input and transform it into a desired output. For example, let us take a pipe to transform a component's birthday property into a human-friendly date using **date** pipe.

```javascript
import { Component } from '@angular/core';

@Component({
    selector: 'app-birthday',
    template: `<p>Birthday is {{ birthday | date }}</p>`
})
export class BirthdayComponent {
    birthday = new Date(1987, 6, 18); // June 18, 1987
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of async pipe</h2>

The AsyncPipe subscribes to an observable or promise and returns the latest value it has emitted. When a new value is emitted, the pipe marks the component to be checked for changes.

Let's take a time observable which continuously updates the view for every 2 seconds with the current time.

```typescript
@Component({
    selector: 'async-observable-pipe',
    template: `<div><code>observable|async</code>:
        Time: {{ time | async }}</div>`
})
export class AsyncObservablePipeComponent {
    time: Observable<string>;
    constructor() {
        this.time = new Observable((observer) => {
            setInterval(() => {
            observer.next(new Date().toString());
            }, 2000);
        });
    }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a parameterized pipe</h2>

A pipe can accept any number of optional parameters to fine-tune its output. The parameterized pipe can be created by declaring the pipe name with a colon ( : ) and then the parameter value. If the pipe accepts multiple parameters, separate the values with colons. Let's take a birthday example with a particular format(dd/MM/yyyy):

```javascript
import { Component } from '@angular/core';

    @Component({
        selector: 'app-birthday',
        template: `<p>Birthday is {{ birthday | date:'dd/MM/yyyy'}}</p>` // 18/06/1987
    })
    export class BirthdayComponent {
        birthday = new Date(1987, 6, 18);
    }
```
**Note:** The parameter value can be any valid template expression, such as a string literal or a component property.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you chain pipes</h2>

You can chain pipes together in potentially useful combinations as per the needs. Let's take a birthday property which uses date pipe(along with parameter) and uppercase pipes as below

```javascript
import { Component } from '@angular/core';

@Component({
    selector: 'app-birthday',
    template: `<p>Birthday is {{  birthday | date:'fullDate' | uppercase}} </p>` // THURSDAY, JUNE 18, 1987
})
export class BirthdayComponent {
    birthday = new Date(1987, 6, 18);
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a custom pipe</h2>

Apart from built-in pipes, you can write your own custom pipe with the below key characteristics:

1. A pipe is a class decorated with pipe metadata `@Pipe` decorator, which you import from the core Angular library

For example,

```javascript
@Pipe({name: 'myCustomPipe'})
```

1. The pipe class implements the **PipeTransform** interface's transform method that accepts an input value followed by optional parameters and returns the transformed value.

The structure of `PipeTransform` would be as below,

```javascript
interface PipeTransform {
    transform(value: any, ...args: any[]): any
}
```

1. The `@Pipe` decorator allows you to define the pipe name that you'll use within template expressions. It must be a valid JavaScript identifier.

```javascript
template: `{{someInputValue | myCustomPipe: someOtherValue}}`
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>Give an example of custom pipe</h2>

You can create custom reusable pipes for the transformation of existing value. For example, let us create a custom pipe for finding file size based on an extension,

```javascript
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({name: 'customFileSizePipe'})
    export class FileSizePipe implements PipeTransform {
    transform(size: number, extension: string = 'MB'): string {
        return (size / (1024 * 1024)).toFixed(2) + extension;
    }
}
```
Now you can use the above pipe in template expression as below,

```javascript
template: `
<h2>Find the size of a file</h2>
<p>Size: {{288966 | customFileSizePipe: 'GB'}}</p>
`
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the difference between pure and impure pipe</h2>

A pure pipe is only called when Angular detects a change in the value or the parameters passed to a pipe. For example, any changes to a primitive input value (String, Number, Boolean, Symbol) or a changed object reference (Date, Array, Function, Object). An impure pipe is called for every change detection cycle no matter whether the value or parameters changes. i.e, An impure pipe is called often, as often as every keystroke or mouse-move.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is slice pipe</h2>

The slice pipe is used to create a new Array or String containing a subset (slice) of the elements. The syntax looks like as below,

```javascript
{{ value_expression | slice : start [ : end ] }}
```

For example, you can provide 'hello' list based on a greeting array,

```javascript
@Component({
    selector: 'list-pipe',
    template: `<ul>
    <li *ngFor="let i of greeting | slice:0:5">{{i}}</li>
    </ul>`
})

export class PipeListComponent {
    greeting: string[] = ['h', 'e', 'l', 'l', 'o', 'm','o', 'r', 'n', 'i', 'n', 'g'];
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the list of template expression operators</h2>

The Angular template expression language supports three special template expression operators.

1. Pipe operator
2. Safe navigation operator
3. Non-null assertion operator

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the precedence between pipe and ternary operators</h2>

The pipe operator has a higher precedence than the ternary operator (?:). For example, the expression `first ? second : third | fourth` is parsed as `first ? second : (third | fourth)`.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How does angular finds components, directives and pipes</h2>

The Angular compiler finds a component or directive in a template when it can match the selector of that component or directive in that template. Whereas it finds a pipe if the pipe's name appears within the pipe syntax of the template HTML.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are Http Interceptors</h2>

Http Interceptors are part of @angular/common/http, which inspect and transform HTTP requests from your application to the server and vice-versa on HTTP responses. These interceptors can perform a variety of implicit tasks, from authentication to logging.

The syntax of HttpInterceptor interface looks like as below,

```javascript
interface HttpInterceptor {
intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>>
}
```
You can use interceptors by declaring a service class that implements the intercept() method of the HttpInterceptor interface.

```javascript
@Injectable()
export class MyInterceptor implements HttpInterceptor {
    constructor() {}
    intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
        ...
    }
}
```
After that you can use it in your module,

```javascript
@NgModule({
    ...
    providers: [
        {
            provide: HTTP_INTERCEPTORS,
            useClass: MyInterceptor,
            multi: true
        }
    ]
    ...
})
export class AppModule {}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the applications of HTTP interceptors</h2>

The HTTP Interceptors can be used for different variety of tasks,

1. Authentication
2. Logging
3. Caching
4. Fake backend
5. URL transformation
6. Modifying headers

**[⬆ Back to Top](#table-of-contents)**

### <h2>How can I use interceptor for an entire application</h2>

You can use same instance of `HttpInterceptors` for the entire app by importing the `HttpClientModule` only in your AppModule, and add the interceptors to the root application injector.

For example, let's define a class that is injectable in root application.

```ts
@Injectable()
export class MyInterceptor implements HttpInterceptor {
    intercept(
        req: HttpRequest<any>,
        next: HttpHandler
    ): Observable<HttpEvent<any>> {

        return next.handle(req).do(event => {
            if (event instanceof HttpResponse) {
                    // Code goes here
            }
        });

    }
}
```
After that import HttpClientModule in AppModule

```ts
@NgModule({
    declarations: [AppComponent],
    imports: [BrowserModule, HttpClientModule],
    providers: [
        { provide: HTTP_INTERCEPTORS, useClass: MyInterceptor, multi: true }
    ],
    bootstrap: [AppComponent]
})
export class AppModule {}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are reactive forms</h2>

Reactive forms is a model-driven approach for creating forms in a reactive style(form inputs changes over time). These are built around observable streams, where form inputs and values are provided as streams of input values. Let's follow the below steps to create reactive forms,

1. Register the reactive forms module which declares reactive-form directives in your app

```js
import { ReactiveFormsModule } from '@angular/forms';

@NgModule({
    imports: [
    // other imports ...
    ReactiveFormsModule
    ],
})
export class AppModule { }
```

2. Create a new FormControl instance and save it in the component.

```js
import { Component } from '@angular/core';
import { FormControl } from '@angular/forms';

@Component({
    selector: 'user-profile',
    styleUrls: ['./user-profile.component.css']
})
export class UserProfileComponent {
    userName = new FormControl('');
}
```

3. Register the FormControl in the template.

```html
<label>
    User name: <input type="text" [formControl]="userName">
</label>
```

Finally, the component with reactive form control appears as below,

```js
import { Component } from '@angular/core';
import { FormControl } from '@angular/forms';

@Component({
 selector: 'user-profile',
 styleUrls: ['./user-profile.component.css'],
 template: `
   <label>
     User name:
     <input type="text" [formControl]="userName">
   </label>
 `
})
export class UserProfileComponent {
 userName = new FormControl('');
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are dynamic forms</h2>

Dynamic forms is a pattern in which we build a form dynamically based on metadata that describes a business object model. You can create them based on reactive form API.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are template driven forms</h2>

Template driven forms are model-driven forms where you write the logic, validations, controls etc, in the template part of the code using directives. They are suitable for simple scenarios and uses two-way binding with [(ngModel)] syntax.

For example, you can create register form easily by following the below simple steps,

1. Import the FormsModule into the Application module's imports array

```js
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import {FormsModule} from '@angular/forms'
import { RegisterComponent } from './app.component';
@NgModule({
    declarations: [
    RegisterComponent,
    ],
    imports: [
    BrowserModule,
    FormsModule
    ],
    providers: [],
    bootstrap: [RegisterComponent]
})
export class AppModule { }
```

2. Bind the form from template to the component using ngModel syntax

```html
<input type="text" class="form-control" id="name" required [(ngModel)]="model.name" name="name">
```

3.  Attach NgForm directive to the <form> tag in order to create FormControl instances and register them

```html
<form #registerForm="ngForm">
```

4. Apply the validation message for form controls

```html
<label for="name">Name</label>
<input type="text" class="form-control" id="name" required [(ngModel)]="model.name" name="name" #name="ngModel">
<div [hidden]="name.valid || name.pristine" class="alert alert-danger">
Please enter your name
</div>
```

5. Let's submit the form with ngSubmit directive and add type="submit" button at the bottom of the form to trigger form submit.

```html
<form (ngSubmit)="onSubmit()" #heroForm="ngForm">
<!-- Form goes here -->
<button type="submit" class="btn btn-success" [disabled]="!registerForm.form.valid">Submit</button>
```

Finally, the completed template-driven registration form will be appeared as follow.

```html
<div class="container">
<h1>Registration Form</h1>
<form (ngSubmit)="onSubmit()" #registerForm="ngForm">
    <div class="form-group">
    <label for="name">Name</label>
        <input type="text" class="form-control" id="name" required [(ngModel)]="model.name" name="name" #name="ngModel">
        <div [hidden]="name.valid || name.pristine" class="alert alert-danger">
            Please enter your name
        </div>
    </div>
    <button type="submit" class="btn btn-success" [disabled]="!registerForm.form.valid">Submit</button>
</form>
</div>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the differences between reactive forms and template driven forms</h2>

Below are the main differences between reactive forms and template driven forms

| Feature                | Reactive                                                          | Template-Driven                                |
| ---------------------- | ----------------------------------------------------------------- | ---------------------------------------------- |
| Form model setup       | Created(FormControl instance) in component explicitly             | Created by directives                          |
| Data updates           | Synchronous                                                       | Asynchronous                                   |
| Form custom validation | Defined as Functions                                              | Defined as Directives                          |
| Testing                | No interaction with change detection cycle                        | Need knowledge of the change detection process |
| Mutability             | Immutable(by always returning new value for FormControl instance) | Mutable(Property always modified to new value) |
| Scalability            | More scalable using low-level APIs                                | Less scalable using due to abstraction on APIs |

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the different ways to group form controls</h2>

Reactive forms provide two ways of grouping multiple related controls.

1. **FormGroup**: It defines a form with a fixed set of controls those can be managed together in an one object. It has same properties and methods similar to a FormControl instance.

This FormGroup can be nested to create complex forms as below.

```js
import { Component } from '@angular/core';
import { FormGroup, FormControl } from '@angular/forms';

@Component({
    selector: 'user-profile',
    templateUrl: './user-profile.component.html',
    styleUrls: ['./user-profile.component.css']
})

export class UserProfileComponent {
    userProfile = new FormGroup({
    firstName: new FormControl(''),
    lastName: new FormControl(''),
    address: new FormGroup({
        street: new FormControl(''),
        city: new FormControl(''),
        state: new FormControl(''),
        zip: new FormControl('')
        })
    });

    onSubmit() {
    // Store this.userProfile.value in DB
    }
}
```
```html
<form [formGroup]="userProfile" (ngSubmit)="onSubmit()">
    <label>First Name: <input type="text" formControlName="firstName"></label>
    <label>Last Name: <input type="text" formControlName="lastName"></label>
    <div formGroupName="address">
        <h3>Address</h3>
        <label>Street: <input type="text" formControlName="street"></label>
        <label>City: <input type="text" formControlName="city"></label>
        <label>State:<input type="text" formControlName="state"></label>
        <label>Zip Code: <input type="text" formControlName="zip"></label>
    </div>
    <button type="submit" [disabled]="!userProfile.valid">Submit</button>
</form>
```

2. **FormArray:** It defines a dynamic form in an array format, where you can add and remove controls at run time. This is useful for dynamic forms when you don’t know how many controls will be present within the group.

```js
import { Component } from '@angular/core';
import { FormArray, FormControl } from '@angular/forms';

@Component({
  selector: 'order-form',
  templateUrl: './order-form.component.html',
  styleUrls: ['./order-form.component.css']
})
export class OrderFormComponent {
  constructor () {
    this.orderForm = new FormGroup({
      firstName: new FormControl('John', Validators.minLength(3)),
      lastName: new FormControl('Rodson'),
      items: new FormArray([
        new FormControl(null)
      ])
    });
  }

  onSubmitForm () {
    // Save the items this.orderForm.value in DB
  }

  onAddItem () {
    this.orderForm.controls
    .items.push(new FormControl(null));
  }

  onRemoveItem (index) {
    this.orderForm.controls['items'].removeAt(index);
  }
}
```
```html
<form [formControlName]="orderForm" (ngSubmit)="onSubmit()">
    <label>First Name: <input type="text" formControlName="firstName"></label>
    <label>Last Name: <input type="text" formControlName="lastName"></label>
    <div>
        <p>Add items</p>
        <ul formArrayName="items">
        <li *ngFor="let item of orderForm.controls.items.controls; let i = index">
            <input type="text" formControlName="{{i}}">
            <button type="button" title="Remove Item" (click)="onRemoveItem(i)">Remove</button>
        </li>
        </ul>
        <button type="button" (click)="onAddItem">Add an item</button>
    </div>
</form>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you update specific properties of a form model</h2>

You can use `patchValue()` method to update specific properties defined in the form model. For example,you can update the name and street of certain profile on click of the update button as shown below.

```js
updateProfile() {
    this.userProfile.patchValue({
        firstName: 'John',
        address: {
        street: '98 Crescent Street'
        }
    });
}
```
```html
<button (click)="updateProfile()">Update Profile</button>
```

You can also use `setValue` method to update properties.

**Note:** Remember to update the properties against the exact model structure.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of FormBuilder</h2>

FormBuilder is used as syntactic sugar for easily creating instances of a FormControl, FormGroup, or FormArray. This is helpful to reduce the amount of boilerplate needed to build complex reactive forms. It is available as an injectable helper class of the `@angular/forms` package.

For example, the user profile component creation becomes easier as shown here.

```js
export class UserProfileComponent {
    profileForm = this.formBuilder.group({
        firstName: [''],
        lastName: [''],
        address: this.formBuilder.group({
            street: [''],
            city: [''],
            state: [''],
            zip: ['']
        }),
    });
    constructor(private formBuilder: FormBuilder) { }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you verify the model changes in forms</h2>

You can add a getter property(let's say, diagnostic) inside component to return a JSON representation of the model during the development. This is useful to verify whether the values are really flowing from the input box to the model and vice versa or not.

```js
export class UserProfileComponent {
    model = new User('John', 29, 'Writer');
    // TODO: Remove after the verification
    get diagnostic() { return JSON.stringify(this.model); }
}
```

and add `diagnostic` binding near the top of the form

```html
{{diagnostic}}
<div class="form-group">
<!-- FormControls goes here -->
</div>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the state CSS classes provided by ngModel</h2>

The ngModel directive updates the form control with special Angular CSS classes to reflect it's state. Let's find the list of classes in a tabular format,

| Form control state | If true    | If false     |
| ------------------ | ---------- | ------------ |
| Visited            | ng-touched | ng-untouched |
| Value has changed  | ng-dirty   | ng-pristine  |
| Value is valid     | ng-valid   | ng-invalid   |

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you reset the form</h2>

- In a model-driven form, you can reset the form just by calling the function `reset()` on our form model.
- For example, you can reset the form model on submission as follows,

```js
onSubmit() {
    if (this.myform.valid) {
        console.log("Form is submitted");
        // Perform business logic here
        this.myform.reset();
    }
}
```
Now, your form model resets the form back to its original pristine state.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the types of validator functions</h2>

In reactive forms, the validators can be either synchronous or asynchronous functions,

1. **Sync validators:** These are the synchronous functions which take a control instance and immediately return either a set of validation errors or null. Also, these functions passed as second argument while instantiating the form control. The main use cases are simple checks like whether a field is empty, whether it exceeds a maximum length etc.

2. **Async validators:** These are the asynchronous functions which take a control instance and return a Promise or Observable that later emits a set of validation errors or null. Also, these functions passed as second argument while instantiating the form control. The main use cases are complex validations like hitting a server to check the availability of a username or email.

The representation of these validators looks like below
```js
this.myForm = formBuilder.group({
   firstName: ['value'],
   lastName: ['value', *Some Sync validation function*],
   email: ['value', *Some validation function*, *Some asynchronous validation function*]
});
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>Can you give an example of built-in validators</h2>

In reactive forms, you can use built-in validator like `required` and `minlength` on your input form controls. For example, the registration form can have these validators on name input field

```js
this.registrationForm = new FormGroup({
    'name': new FormControl(this.hero.name, [
    Validators.required,
    Validators.minLength(4),
    ])
});
```
Whereas in template-driven forms, both `required` and `minlength` validators available as attributes.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you optimize the performance of async validators</h2>

Since all validators run after every form value change, it creates a major impact on performance with async validators by hitting the external API on each keystroke. This situation can be avoided by delaying the form validity by changing the updateOn property from change (default) to submit or blur.

The usage would be different based on form types,

1. **Template-driven forms:** Set the property on `ngModelOptions` directive

```html
<input [(ngModel)]="name" [ngModelOptions]="{updateOn: 'blur'}">
```

2. **Reactive-forms:** Set the property on FormControl instance

```js
name = new FormControl('', {updateOn: 'blur'});
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is Angular Router</h2>

Angular Router is a mechanism in which navigation happens from one view to the next as users perform application tasks. It borrows the concepts or model of browser's application navigation. It enables developers to build Single Page Applications with multiple views and allow navigation between these views.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of base href tag</h2>

The routing application should add <base> element to the index.html as the first child in the <head> tag in order to indicate how to compose navigation URLs. If app folder is the application root then you can set the href value as below

```html
<base href="/">
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the router imports</h2>

The Angular Router which represents a particular component view for a given URL is not part of Angular Core. It is available in library named `@angular/router` to import required router components. For example, we import them in app module as below,

```javascript
import { RouterModule, Routes } from '@angular/router';
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is router outlet</h2>

The RouterOutlet is a directive from the router library and it  acts as a placeholder that marks the spot in the template where the router should display the components for that outlet. Router outlet is used like a component,

```html
<router-outlet></router-outlet>
<!-- Routed components go here -->
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are router links</h2>

The RouterLink is a directive on the anchor tags give the router control over those elements. Since the navigation paths are fixed, you can assign string values to router-link directive as below,

```html
<h1>Angular Router</h1>
<nav>
    <a routerLink="/todosList" >List of todos</a>
    <a routerLink="/completed" >Completed todos</a>
</nav>
<router-outlet></router-outlet>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are active router links</h2>

RouterLinkActive is a directive that toggles css classes for active RouterLink bindings based on the current RouterState. i.e, The Router will add CSS classes when this link is active and remove when the link is inactive. For example, you can add them to RouterLinks as below.

```html
<h1>Angular Router</h1>
<nav>
    <a routerLink="/todosList" routerLinkActive="active">List of todos</a>
    <a routerLink="/completed" routerLinkActive="active">Completed todos</a>
</nav>
<router-outlet></router-outlet>
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is router state</h2>

RouterState is a tree of activated routes. Every node in this tree knows about the "consumed" URL segments, the extracted parameters, and the resolved data. You can access the current RouterState from anywhere in the application using the `Router service` and the `routerState` property.

```javascript
@Component({templateUrl:'template.html'})
class MyComponent {
    constructor(router: Router) {
    const state: RouterState = router.routerState;
    const root: ActivatedRoute = state.root;
    const child = root.firstChild;
    const id: Observable<string> = child.params.map(p => p.id);
    //...
    }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are router events</h2>

During each navigation, the Router emits navigation events through the Router.events property allowing you to track the lifecycle of the route.

The sequence of router events is as below,

1. NavigationStart,
2. RouteConfigLoadStart,
3. RouteConfigLoadEnd,
4. RoutesRecognized,
5. GuardsCheckStart,
6. ChildActivationStart,
7. ActivationStart,
8. GuardsCheckEnd,
9. ResolveStart,
10. ResolveEnd,
11. ActivationEnd
12. ChildActivationEnd
13. NavigationEnd,
14. NavigationCancel,
15. NavigationError
16. Scroll

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is activated route</h2>

ActivatedRoute contains the information about a route associated with a component loaded in an outlet. It can also be used to traverse the router state tree. The ActivatedRoute will be injected as a router service to access the information. In the below example, you can access route path and parameters,

```javascript
@Component({...})
class MyComponent {
    constructor(route: ActivatedRoute) {
        const id: Observable<string> = route.params.pipe(map(p => p.id));
        const url: Observable<string> = route.url.pipe(map(segments => segments.join('')));
        // route.data includes both `data` and `resolve`
        const user = route.data.pipe(map(d => d.user));
    }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you define routes</h2>

A router must be configured with a list of route definitions. You configures the router with routes via the `RouterModule.forRoot()` method, and adds the result to the AppModule's `imports` array.

```javascript
const appRoutes: Routes = [
    { path: 'todo/:id',      component: TodoDetailComponent },
    { path: 'todos', component: TodosListComponent, data: { title: 'Todos List' }},
    { path: '', redirectTo: '/todos', pathMatch: 'full' },
    { path: '**', component: PageNotFoundComponent }
];

@NgModule({
    imports: [
        RouterModule.forRoot(
            appRoutes,
            { enableTracing: true } // <-- debugging purposes only
        )
        // other imports here
    ],
    ...
})
export class AppModule { }
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of Wildcard route</h2>

If the URL doesn't match any predefined routes then it causes the router to throw an error and crash the app. In this case, you can use wildcard route. A wildcard route has a path consisting of two asterisks to match every URL.

For example, you can define PageNotFoundComponent for wildcard route as below

```javascript
{ path: '**', component: PageNotFoundComponent }
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>Do I need a Routing Module always</h2>

No, the Routing Module is a design choice. You can skip routing Module (for example, AppRoutingModule) when the configuration is simple and merge the routing configuration directly into the companion module (for example, AppModule). But it is recommended when the configuration is complex and includes specialized guard and resolver services.


**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you detect route change in Angular</h2>

In Angular7, you can subscribe to router to detect the changes. The subscription for router events would be as below,

```javascript
this.router.events.subscribe((event: Event) => {})
```
Let's take a simple component to detect router changes

```javascript
import { Component } from '@angular/core';
import { Router, Event, NavigationStart, NavigationEnd, NavigationError } from '@angular/router';

@Component({
    selector: 'app-root',
    template: `<router-outlet></router-outlet>`
})
export class AppComponent {

    constructor(private router: Router) {

        this.router.events.subscribe((event: Event) => {
            if (event instanceof NavigationStart) {
                // Show loading indicator and perform an action
            }

            if (event instanceof NavigationEnd) {
                // Hide loading indicator and perform an action
            }

            if (event instanceof NavigationError) {
                // Hide loading indicator and perform an action
                console.log(event.error); // It logs an error for debugging
            }
        });
    }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How can I use SASS in angular project</h2>

When you are creating your project with angular cli, you can use `ng new`command. It generates all your components with predefined sass files.

```javascript
ng new My_New_Project --style=sass
```

But if you are changing your existing style in your project then use `ng set` command,

```javascript
ng set defaults.styleExt scss
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you get the current route</h2>

In Angular, there is an `url` property of router package to get the current route. You need to follow the below few steps,

1. Import Router from @angular/router

```js
import { Router } from '@angular/router';
```

2. Inject router inside constructor

```js
constructor(private router: Router ) {

}
```
3. Access url parameter

```js
console.log(this.router.url); //  /routename
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>Is Angular supports dynamic imports</h2>

Yes, Angular 8 supports dynamic imports in router configuration. i.e, You can use the import statement for lazy loading the module using `loadChildren` method and it will be understood by the IDEs(VSCode and WebStorm), webpack, etc.

Previously, you have been written as below to lazily load the feature module. By mistake, if you have typo in the module name it still accepts the string and throws an error during build time.

```javascript
{path: ‘user’, loadChildren: ‘./users/user.module#UserModulee’},
```

This problem is resolved by using dynamic imports and IDEs are able to find it during compile time itself.

```javascript
{path: ‘user’, loadChildren: () => import(‘./users/user.module’).then(m => m.UserModule)};
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is lazy loading</h2>

Lazy loading is one of the most useful concepts of Angular Routing. It helps us to download the web pages in chunks instead of downloading everything in a big bundle. It is used for lazy loading by asynchronously loading the feature module for routing whenever required using the property `loadChildren`. Let's load both `Customer` and `Order` feature modules lazily as below,

```javascript
const routes: Routes = [
    {
        path: 'customers',
        loadChildren: () => import('./customers/customers.module').then(module => module.CustomersModule)
    },
    {
        path: 'orders',
        loadChildren: () => import('./orders/orders.module').then(module => module.OrdersModule)
    },
    {
        path: '',
        redirectTo: '',
        pathMatch: 'full'
    }
];
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are different types of compilation in Angular</h2>

Angular offers two ways to compile your application,

1. Just-in-Time (JIT)
2. Ahead-of-Time (AOT)

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is JIT</h2>

Just-in-Time (JIT) is a type of compilation that compiles your app in the browser at runtime. JIT compilation was the default until Angular 8, now default is AOT. When you run the ng build (build only) or ng serve (build and serve locally) CLI commands, the type of compilation (JIT or AOT) depends on the value of the aot property in your build configuration specified in angular.json. By default, aot is set to true.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is AOT</h2>

Ahead-of-Time (AOT) is a type of compilation that compiles your app at build time. This is the default starting in Angular 9. When you run the ng build (build only) or ng serve (build and serve locally) CLI commands, the type of compilation (JIT or AOT) depends on the value of the aot property in your build configuration specified in angular.json. By default, aot is set to true.

```cmd
ng build
ng serve
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is AOT compiler</h2>

The AOT compiler is part of a build process that produces a small, fast, ready-to-run application package, typically for production. It converts your Angular HTML and TypeScript code into efficient JavaScript code during the build phase before the browser downloads and runs that code.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Why do we need compilation process</h2>

The Angular components and templates cannot be understood by the browser directly. Due to that Angular applications require a compilation process before they can run in a browser. For example, In AOT compilation, both Angular HTML and TypeScript code converted into efficient JavaScript code during the build phase before browser runs it.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the advantages with AOT</h2>

Below are the list of AOT benefits,

1. **Faster rendering:** The browser downloads a pre-compiled version of the application. So it can render the application immediately without compiling the app.
2. **Fewer asynchronous requests:** It inlines external HTML templates and CSS style sheets within the application javascript which eliminates separate ajax requests.
3. **Smaller Angular framework download size:** Doesn't require downloading the Angular compiler. Hence it dramatically reduces the application payload.
4. **Detect template errors earlier:** Detects and reports template binding errors during the build step itself
5. **Better security:** It compiles HTML templates and components into JavaScript.  So there won't be any injection attacks.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the ways to control AOT compilation</h2>

You can control your app compilation in two ways,

1. By providing template compiler options in the `tsconfig.json` file
2. By configuring Angular metadata with decorators

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the three phases of AOT</h2>

The AOT compiler works in three phases,

1. **Code Analysis:** The compiler records a representation of the source
2. **Code generation:** It handles the interpretation as well as places restrictions on what it interprets.
3. **Validation:** In this phase, the Angular template compiler uses the TypeScript compiler to validate the binding expressions in templates.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Can I use arrow functions in AOT</h2>

No, Arrow functions or lambda functions can’t be used to assign values to the decorator properties. For example, the following snippet is invalid:

```javascript
@Component({
    providers: [{
    provide: MyService, useFactory: () => getService()
    }]
})
```

To fix this, it has to be changed as following exported function:

```javascript
function getService(){
    return new MyService();
}

@Component({
    providers: [{
    provide: MyService, useFactory: getService
    }]
})
```

If you still use arrow function, it generates an error node in place of the function. When the compiler later interprets this node, it reports an error to turn the arrow function into an exported function.

**Note:** From Angular5 onwards, the compiler automatically performs this rewriting while emitting the .js file.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Can I use any javascript feature for expression syntax in AOT</h2>

No, the AOT collector understands a subset  of (or limited) JavaScript features. If an expression uses unsupported syntax, the collector writes an error node to the .metadata.json file. Later point of time, the compiler reports an error if it needs that piece of metadata to generate the application code.

**[⬆ Back to Top](#table-of-contents)**




<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
