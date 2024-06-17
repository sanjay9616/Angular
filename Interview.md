<h1>Angular Interview Questions and Answers</h1>

### Table of Contents

| No. | Questions                                                                                                                                                                                   |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is Angular Framework](#What-is-Angular-Framework)                                                                                                                                     |
| 1   | [How do you find angular CLI version](#How-do-you-find-angular-CLI-version)                                                                                                                 |
| 1   | [How do you upgrade angular version](#How-do-you-upgrade-angular-version)                                                                                                                   |
| 1   | [What is the difference between AngularJS and Angular](#What-is-the-difference-between-AngularJS-and-Angular)                                                                               |
| 1   | [What is TypeScript](#What-is-TypeScript)                                                                                                                                                   |
| 1   | [Write a pictorial diagram of Angular architecture](#Write-a-pictorial-diagram-of-Angular-architecture)                                                                                     |
| 1   | [What are the key components of Angular](#What-are-the-key-components-of-Angular)                                                                                                           |
| 1   | [What are components](#What-are-components)                                                                                                                                                 |
| 1   | [What is a template](#What-is-a-template)                                                                                                                                                   |
| 1   | [What is Angular CLI](#What-is-Angular-CLI)                                                                                                                                                 |
| 1   | [What is Angular CLI Builder](#What-is-Angular-CLI-Builder)                                                                                                                                 |
| 1   | [What is a builder](#What-is-a-builder)                                                                                                                                                     |
| 1   | [How do you invoke a builder](#How-do-you-invoke-a-builder)                                                                                                                                 |
| 1   | [What is dependency injection in Angular](#What-is-dependency-injection-in-Angular)                                                                                                         |
| 1   | [How is Dependency Hierarchy formed](#How-is-Dependency-Hierarchy-formed)                                                                                                                   |
| 1   | [What is the option to choose between inline and external template file](#What-is-the-option-to-choose-between-inline-and-external-template-file)                                           |
| 1   | [What happens if you use script tag inside template](#What-happens-if-you-use-script-tag-inside-template)                                                                                   |
| 1   | [What are template expressions](#What-are-template-expressions)                                                                                                                             |
| 1   | [What are template statements](#What-are-template-statements)                                                                                                                               |
| 1   | [What are Angular elements](#What-are-Angular-elements)                                                                                                                                     |
| 1   | [What is the browser support of Angular Elements](#What-is-the-browser-support-of-Angular-Elements)                                                                                         |
| 1   | [What are custom elements](#What-are-custom-elements)                                                                                                                                       |
| 1   | [Do I need to bootstrap custom elements](#Do-I-need-to-bootstrap-custom-elements)                                                                                                           |
| 1   | [Explain how custom elements works internally](#Explain-how-custom-elements-works-internally)                                                                                               |
| 1   | [How to transfer components to custom elements](#How-to-transfer-components-to-custom-elements)                                                                                             |
| 1   | [What are the mapping rules between Angular component and custom element](#What-are-the-mapping-rules-between-Angular-component-and-custom-element)                                         |
| 1   | [How do you define typings for custom elements](#How-do-you-define-typings-for-custom-elements)                                                                                             |
| 1   | [What are dynamic components](#What-are-dynamic-components)                                                                                                                                 |
| 1   | [What is Angular Universal](#What-is-Angular-Universal)                                                                                                                                     |
| 1   | [What is content projection](#What-is-content-projection)                                                                                                                                   |
| 1   | [What is ng-content and its purpose](#What-is-ng-content-and-its-purpose)                                                                                                                   |
| 1   | [How do you select an element in component template](#How-do-you-select-an-element-in-component-template)                                                                                   |
| 1   | [What is standalone component](#What-is-standalone-component)                                                                                                                               |
| 1   | [How to create a standalone component using CLI command](#How-to-create-a-standalone-component-using-CLI-command)                                                                           |
| 1   | [What is hydration](#What-is-hydration)                                                                                                                                                     |
| 1   | [What is a data binding](#What-is-a-data-binding)                                                                                                                                           |
| 2   | [What is interpolation](#What-is-interpolation)                                                                                                                                             |
| 3   | [How do you categorize data binding types](#How-do-you-categorize-data-binding-types)                                                                                                       |
| 4   | [What is the difference between interpolated content and innerHTM](#What-is-the-difference-between-interpolated-content-and-innerHTM)                                                       |
| 5   | [What are lifecycle hooks available](#What-are-lifecycle-hooks-available)                                                                                                                   |
| 6   | [What is the difference between constructor and ngOnInit](#What-is-the-difference-between-constructor-and-ngOnInit)                                                                         |
| 7   | [What are the lifecycle hooks of a zone](#What-are-the-lifecycle-hooks-of-a-zone)                                                                                                           |
| 8   | [What are directives](#What-are-directives)                                                                                                                                                 |
| 9   | [What are the differences between Component and Directive](#What-are-the-differences-between-Component-and-Directive)                                                                       |
| 10  | [What is the purpose of *ngFor directive](#What-is-the-purpose-of-*ngFor-directive)                                                                                                         |
| 11  | [What is the purpose of *ngIf directive](#What-is-the-purpose-of-*ngIf-directive)                                                                                                           |
| 12  | [What are the various kinds of directives](#What-are-the-various-kinds-of-directives)                                                                                                       |
| 13  | [How do you create directives using CLI](#How-do-you-create-directives-using-CLI)                                                                                                           |
| 14  | [Give an example for attribute directives](#Give-an-example-for-attribute-directives)                                                                                                       |
| 15  | [What is the purpose of hidden property](#What-is-the-purpose-of-hidden-property)                                                                                                           |
| 16  | [What is the difference between ngIf and hidden property](#What-is-the-difference-between-ngIf-and-hidden-property)                                                                         |
| 17  | [What is index property in ngFor directive](#What-is-index-property-in-ngFor-directive)                                                                                                     |
| 18  | [What is the purpose of ngFor trackBy](#What-is-the-purpose-of-ngFor-trackBy)                                                                                                               |
| 19  | [What is the purpose of ngSwitch directive](#What-is-the-purpose-of-ngSwitch-directive)                                                                                                     |
| 20  | [How to set ngFor and ngIf on the same element](#How-to-set-ngFor-and-ngIf-on-the-same-element)                                                                                             |
| 4   | [What is host property in css](#What-is-host-property-in-css)                                                                                                                               |
| 4   | [What is metadata](#What-is-metadata)                                                                                                                                                       |
| 4   | [What are the restrictions of metadata](#What-are-the-restrictions-of-metadata)                                                                                                             |
| 4   | [What is the purpose of metadata json files](#What-is-the-purpose-of-metadata-json-files)                                                                                                   |
| 4   | [Give an example of few metadata errors](#Give-an-example-of-few-metadata-errors)                                                                                                           |
| 4   | [What is metadata rewriting](#What-is-metadata-rewriting)                                                                                                                                   |
| 4   | [What is the role of ngModule metadata in compilation process](#What-is-the-role-of-ngModule-metadata-in-compilation-process)                                                               |
| 4   | [What is a service](#What-is-a-service)                                                                                                                                                     |
| 4   | [What are class field decorators](#What-are-class-field-decorators)                                                                                                                         |
| 4   | [What are the class decorators in Angular](#What-are-the-class-decorators-in-Angular)                                                                                                       |
| 4   | [Is it possible to do aliasing for inputs and outputs](#Is-it-possible-to-do-aliasing-for-inputs-and-outputs)                                                                               |
| 4   | [What is a module](#What-is-a-module)                                                                                                                                                       |
| 4   | [What are feature modules](#What-are-feature-modules)                                                                                                                                       |
| 4   | [What are the types of feature modules](#What-are-the-types-of-feature-modules)                                                                                                             |
| 4   | [What are the imported modules in CLI generated feature modules](#What-are-the-imported-modules-in-CLI-generated-feature-modules)                                                           |
| 4   | [What is the purpose of common module](#What-is-the-purpose-of-common-module)                                                                                                               |
| 4   | [What is Angular Material](#What-is-Angular-Material)                                                                                                                                       |
| 4   | [What happens if browserModule used in feature module](#What-happens-if-browserModule-used-in-feature-module)                                                                               |
| 4   | [What happens if I import the same module twice](#What-happens-if-I-import-the-same-module-twice)                                                                                           |
| 4   | [How does forRoot method helpful to avoid duplicate router instances](#How-does-forRoot-method-helpful-to-avoid-duplicate-router-instances)                                                 |
| 4   | [What are the differences between ngmodule and javascript module](#What-are-the-differences-between-ngmodule-and-javascript-module)                                                         |
| 4   | [Give few examples for NgModules](#Give-few-examples-for-NgModules)                                                                                                                         |
| 4   | [What is declarable in Angular](#What-is-declarable-in-Angular)                                                                                                                             |
| 4   | [What are the restrictions on declarable classes](#What-are-the-restrictions-on-declarable-classes)                                                                                         |
| 4   | [What classes should not be added to declarations](#What-classes-should-not-be-added-to-declarations)                                                                                       |
| 4   | [What are the possible errors with declarations](#What-are-the-possible-errors-with-declarations)                                                                                           |
| 4   | [What are the steps to use declaration elements](#What-are-the-steps-to-use-declaration-elements)                                                                                           |
| 4   | [What is a provider](#What-is-a-provider)                                                                                                                                                   |
| 4   | [What is the recommendation for provider scope](#What-is-the-recommendation-for-provider-scope)                                                                                             |
| 4   | [How do you configure injectors with providers at different levels](#How-do-you-configure-injectors-with-providers-at-different-levels)                                                     |
| 4   | [How do you restrict provider scope to a module](#How-do-you-restrict-provider-scope-to-a-module)                                                                                           |
| 4   | [What is the reason for No provider for HTTP exception](#What-is-the-reason-for-No-provider-for-HTTP-exception)                                                                             |
| 4   | [What is a bootstrapping module](#What-is-a-bootstrapping-module)                                                                                                                           |
| 4   | [What is a bootstrapped component](#What-is-a-bootstrapped-component)                                                                                                                       |
| 4   | [How do you manually bootstrap an application](#How-do-you-manually-bootstrap-an-application)                                                                                               |
| 4   | [Is it necessary for bootstrapped component to be entry component](#Is-it-necessary-for-bootstrapped-component-to-be-entry-component)                                                       |
| 4   | [Why is not necessary to use entryComponents array every time](#Why-is-not-necessary-to-use-entryComponents-array-every-time)                                                               |
| 4   | [Do I still need to use entryComponents array in Angular9](#Do-I-still-need-to-use-entryComponents-array-in-Angular9)                                                                       |
| 4   | [What is a routed entry component](#What-is-a-routed-entry-component)                                                                                                                       |
| 4   | [What is an entry component](#What-is-an-entry-component)                                                                                                                                   |
| 4   | [What is a shared module](#What-is-a-shared-module)                                                                                                                                         |
| 4   | [Can I share services using modules](#Can-I-share-services-using-modules)                                                                                                                   |
| 4   | [How do you provide a singleton service](#How-do-you-provide-a-singleton-service)                                                                                                           |
| 4   | [What are the different ways to remove duplicate service registration](#What-are-the-different-ways-to-remove-duplicate-service-registration)                                               |
| 4   | [Is it mandatory to use injectable on every service class](#Is-it-mandatory-to-use-injectable-on-every-service-class)                                                                       |
| 4   | [What are the types of injector hierarchies](#What-are-the-types-of-injector-hierarchies)                                                                                                   |
| 4   | [How to inject the dynamic script in angular](#How-to-inject-the-dynamic-script-in-angular)                                                                                                 |
| 4   | [What are the differences between AngularJS and Angular with respect to dependency injection](#What-are-the-differences-between-AngularJS-and-Angular-with-respect-to-dependency-injection) |
| 4   | [What is HttpClient and its benefits](#What-is-HttpClient-and-its-benefits)                                                                                                                 |
| 4   | [Explain on how to use HttpClient with an example](#Explain-on-how-to-use-HttpClient-with-an-example)                                                                                       |
| 4   | [How can you read full response](#How-can-you-read-full-response)                                                                                                                           |
| 4   | [How do you perform Error handling](#How-do-you-perform-Error-handling)                                                                                                                     |
| 4   | [How do you pass headers for HTTP client](#How-do-you-pass-headers-for-HTTP-client)                                                                                                         |
| 4   | [Is angular prevents http level vulnerabilities](#Is-angular-prevents-http-level-vulnerabilities)                                                                                           |
| 4   | [What is angular animation](#What-is-angular-animation)                                                                                                                                     |
| 4   | [What are the steps to use animation module](#What-are-the-steps-to-use-animation-module)                                                                                                   |
| 4   | [How do you trigger an animation](#How-do-you-trigger-an-animation)                                                                                                                         |
| 4   | [What are pipes](#What-are-pipes)                                                                                                                                                           |
| 4   | [What is the purpose of async pipe](#What-is-the-purpose-of-async-pipe)                                                                                                                     |
| 4   | [What is a parameterized pipe](#What-is-a-parameterized-pipe)                                                                                                                               |
| 4   | [How do you chain pipes](#How-do-you-chain-pipes)                                                                                                                                           |
| 4   | [What is a custom pipe](#What-is-a-custom-pipe)                                                                                                                                             |
| 4   | [Give an example of custom pipe](#Give-an-example-of-custom-pipe)                                                                                                                           |
| 4   | [What is the difference between pure and impure pipe](#What-is-the-difference-between-pure-and-impure-pipe)                                                                                 |
| 4   | [What is slice pipe](#What-is-slice-pipe)                                                                                                                                                   |
| 4   | [What are the list of template expression operators](#What-are-the-list-of-template-expression-operators)                                                                                   |
| 4   | [What is the precedence between pipe and ternary operators](#What-is-the-precedence-between-pipe-and-ternary-operators)                                                                     |
| 4   | [How does angular finds components, directives and pipes](#How-does-angular-finds-components,-directives-and-pipes)                                                                         |
| 4   | [What are Http Interceptors](#What-are-Http-Interceptors)                                                                                                                                   |
| 4   | [What are the applications of HTTP interceptors](#What-are-the-applications-of-HTTP-interceptors)                                                                                           |
| 4   | [How can I use interceptor for an entire application](#How-can-I-use-interceptor-for-an-entire-application)                                                                                 |
| 4   | [What are reactive forms](#What-are-reactive-forms)                                                                                                                                         |
| 4   | [What are dynamic forms](#What-are-dynamic-forms)                                                                                                                                           |
| 4   | [What are template driven forms](#What-are-template-driven-forms)                                                                                                                           |
| 4   | [What are the differences between reactive forms and template driven forms](#What-are-the-differences-between-reactive-forms-and-template-driven-forms)                                     |
| 4   | [What are the different ways to group form controls](#What-are-the-different-ways-to-group-form-controls)                                                                                   |
| 4   | [How do you update specific properties of a form model](#How-do-you-update-specific-properties-of-a-form-model)                                                                             |
| 4   | [What is the purpose of FormBuilder](#What-is-the-purpose-of-FormBuilder)                                                                                                                   |
| 4   | [How do you verify the model changes in forms](#How-do-you-verify-the-model-changes-in-forms)                                                                                               |
| 4   | [What are the state CSS classes provided by ngModel](#What-are-the-state-CSS-classes-provided-by-ngModel)                                                                                   |
| 4   | [How do you reset the form](#How-do-you-reset-the-form)                                                                                                                                     |
| 4   | [What are the types of validator functions](#What-are-the-types-of-validator-functions)                                                                                                     |
| 4   | [Can you give an example of built-in validators](#Can-you-give-an-example-of-built-in-validators)                                                                                           |
| 4   | [How do you optimize the performance of async validators](#How-do-you-optimize-the-performance-of-async-validators)                                                                         |
| 4   | [What is Angular Router](#What-is-Angular-Router)                                                                                                                                           |
| 4   | [What is the purpose of base href tag](#What-is-the-purpose-of-base-href-tag)                                                                                                               |
| 4   | [What are the router imports](#What-are-the-router-imports)                                                                                                                                 |
| 4   | [What is router outlet](#What-is-router-outlet)                                                                                                                                             |
| 4   | [What are router links](#What-are-router-links)                                                                                                                                             |
| 4   | [What are active router links](#What-are-active-router-links)                                                                                                                               |
| 4   | [What is router state](#What-is-router-state)                                                                                                                                               |
| 4   | [What are router events](#What-are-router-events)                                                                                                                                           |
| 4   | [What is activated route](#What-is-activated-route)                                                                                                                                         |
| 4   | [How do you define routes](#How-do-you-define-routes)                                                                                                                                       |
| 4   | [What is the purpose of Wildcard route](#What-is-the-purpose-of-Wildcard-route)                                                                                                             |
| 4   | [Do I need a Routing Module always](#Do-I-need-a-Routing-Module-always)                                                                                                                     |
| 4   | [How do you detect route change in Angular](#How-do-you-detect-route-change-in-Angular)                                                                                                     |
| 4   | [How can I use SASS in angular project](#How-can-I-use-SASS-in-angular-project)                                                                                                             |
| 4   | [How do you get the current route](#How-do-you-get-the-current-route)                                                                                                                       |
| 4   | [Is Angular supports dynamic imports](#Is-Angular-supports-dynamic-imports)                                                                                                                 |
| 4   | [What is lazy loading](#What-is-lazy-loading)                                                                                                                                               |
| 4   | [What are different types of compilation in Angular](#What-are-different-types-of-compilation-in-Angular)                                                                                   |
| 4   | [What is JIT](#What-is-JIT)                                                                                                                                                                 |
| 4   | [What is AOT](#What-is-AOT)                                                                                                                                                                 |
| 4   | [What is AOT compiler](#What-is-AOT-compiler)                                                                                                                                               |
| 4   | [Why do we need compilation process](#Why-do-we-need-compilation-process)                                                                                                                   |
| 4   | [What are the advantages with AOT](#What-are-the-advantages-with-AOT)                                                                                                                       |
| 4   | [What are the ways to control AOT compilation](#What-are-the-ways-to-control-AOT-compilation)                                                                                               |
| 4   | [What are the three phases of AOT](#What-are-the-three-phases-of-AOT)                                                                                                                       |
| 4   | [Can I use arrow functions in AOT](#Can-I-use-arrow-functions-in-AOT)                                                                                                                       |
| 4   | [Can I use any javascript feature for expression syntax in AOT](#Can-I-use-any-javascript-feature-for-expression-syntax-in-AOT)                                                             |
| 4   | [What is Angular Ivy](#What-is-Angular-Ivy)                                                                                                                                                 |
| 4   | [What are the features included in ivy preview](#What-are-the-features-included-in-ivy-preview)                                                                                             |
| 4   | [Can I use AOT compilation with Ivy](#Can-I-use-AOT-compilation-with-Ivy)                                                                                                                   |
| 4   | [What is Angular Language Service](#What-is-Angular-Language-Service)                                                                                                                       |
| 4   | [How do you install angular language service in the project](#How-do-you-install-angular-language-service-in-the-project)                                                                   |
| 4   | [Is there any editor support for Angular Language Service](#Is-there-any-editor-support-for-Angular-Language-Service)                                                                       |
| 4   | [Explain the features provided by Angular Language Service](#Explain-the-features-provided-by-Angular-Language-Service)                                                                     |
| 4   | [What is Bazel tool](#What-is-Bazel-tool)                                                                                                                                                   |
| 4   | [What are the advantages of Bazel tool](#What-are-the-advantages-of-Bazel-tool)                                                                                                             |
| 4   | [How do you use Bazel with Angular CLI](#How-do-you-use-Bazel-with-Angular-CLI)                                                                                                             |
| 4   | [How do you run Bazel directly](#How-do-you-run-Bazel-directly)                                                                                                                             |
| 4   | [What is schematic](#What-is-schematic)                                                                                                                                                     |
| 4   | [What is rule in Schematics](#What-is-rule-in-Schematics)                                                                                                                                   |
| 4   | [What is Schematics CLI](#What-is-Schematics-CLI)                                                                                                                                           |
| 4   | [How do you create schematics for libraries](#How-do-you-create-schematics-for-libraries)                                                                                                   |

### <h2>What is Angular Framework</h2>

Angular is a **TypeScript-based open-source** front-end platform that makes it easy to build web, mobile and desktop applications. The major features of this framework include declarative templates, dependency injection, end to end tooling which ease application development.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you find angular CLI version</h2>

Angular CLI provides it's installed version using below different ways using ng command,

```bash
ng v
ng version
ng -v
ng --version
```
and the output would be as below,

```bash
Angular CLI: 1.6.3
Node: 8.11.3
OS: darwin x64
Angular:
...
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you upgrade angular version</h2>

The Angular upgrade is quite easier using Angular CLI `ng update` command as mentioned below. For example, if you upgrade from Angular 7 to 8 then your lazy loaded route imports will be migrated to the new import syntax automatically.

```bash
$ ng update @angular/cli @angular/core
```

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

### <h2>What is Angular CLI Builder</h2>

In Angular8, the CLI Builder API is stable and available to developers who want to customize the `Angular CLI` by adding or modifying commands. For example, you could supply a builder to perform an entirely new task, or to change which third-party tool is used by an existing command.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a builder</h2>

A builder function is a function that uses the `Architect API` to perform a complex process such as "build" or "test". The builder code is defined in an npm package. For example, BrowserBuilder runs a webpack build for a browser target and KarmaBuilder starts the Karma server and runs a webpack build for unit tests.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you invoke a builder</h2>

The Angular CLI command `ng run` is used to invoke a builder with a specific target configuration. The workspace configuration file, `angular.json`, contains default configurations for built-in builders.

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

### <h2>What is content projection</h2>

Content projection is a pattern in which you insert, or project, the content you want to use inside another component.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is ng-content and its purpose</h2>

The ng-content is used to insert the content dynamically inside the component that helps to increase component reusability.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you select an element in component template</h2>

You can control any DOM element via ElementRef by injecting it into your component's constructor. i.e, The component should have constructor with ElementRef parameter,

```javascript
constructor(myElement: ElementRef) {
    el.nativeElement.style.backgroundColor = 'yellow';
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is standalone component</h2>

A standalone component is a type of component which is not part of any Angular module. It provides a simplified way to build Angular applications.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How to create a standalone component using CLI command</h2>

Generate standalone component using CLI command as shown below

```bash
ng generate component component-name --standalone
```

On running the command standalone component is created.
Here is the list of file created.

1. `component-name.component.ts`
2. `component-name.component.css`
3. `component-name.component.spec`
4. `component-name.component.html`

Next need to update `app.module.ts` as shown below.

```typescript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { ComponentNameComponent } from './component-name/component-name.component';

@NgModule({
imports: [
    BrowserModule,
    ComponentNameComponent
],
declarations: [AppComponent],
bootstrap: [AppComponent],
})
export class AppModule {}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is hydration</h2>

Hydration is the process that restores the server side rendered application on the client. This includes things like reusing the server rendered DOM structures, persisting the application state, transferring application data that was retrieved already by the server, and other processes.

To enable hydration, we have to enable server side rendering or Angular Universal. Once enabled, we can add the following piece of code in the root component.

```typescript
import { bootstrapApplication, provideClientHydration } from '@angular/platform-browser';

bootstrapApplication(RootCmp, {
    providers: [provideClientHydration()]
});
```
Alternatively we can add `providers: [provideClientHydration()]` in the App Module
```typescript
import {provideClientHydration} from '@angular/platform-browser';
import {NgModule} from '@angular/core';
​
@NgModule({
declarations: [RootCmp],
exports: [RootCmp],
bootstrap: [RootCmp],
providers: [provideClientHydration()],
})
export class AppModule {}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How to create a standalone component manually</h2>

To make existing component to standalone, then add `standalone: true` in `component-name.component.ts` as shown below

```typescript
import { CommonModule } from '@angular/common';
import { Component, OnInit } from '@angular/core';

@Component({
standalone: true,
imports: [CommonModule],
selector: 'app-standalone-component',
templateUrl: './standalone-component.component.html',
styleUrls: ['./standalone-component.component.css'],
})
export class ComponentNameComponent implements OnInit {
constructor() {}

ngOnInit() {}
}
```
Next need to update `app.module.ts` as shown below.

```typescript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { ComponentNameComponent } from './component-name/component-name.component';

@NgModule({
imports: [
    BrowserModule,
    ComponentNameComponent
],
declarations: [AppComponent],
bootstrap: [AppComponent],
})
export class AppModule {}
```

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

### <h2>What is a module</h2>

Modules are logical boundaries in your application and the application is divided into separate modules to separate the functionality of your application.

Lets take an example of **app.module.ts** root module declared with **@NgModule** decorator as below,

```typescript
import { NgModule }      from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent }  from './app.component';

@NgModule ({
    imports:      [ BrowserModule ],
    declarations: [ AppComponent ],
    bootstrap:    [ AppComponent ],
    providers: []
})
export class AppModule { }
```

The NgModule decorator has five important (among all) options:
1. The imports option is used to import other dependent modules. The BrowserModule is required by default for any web based angular application.
2. The declarations option is used to define components in the respective module.
3. The bootstrap option tells Angular which Component to bootstrap in the application.
4. The providers option is used to configure a set of injectable objects that are available in the injector of this module.
5. The entryComponents option is a set of components dynamically loaded into the view.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are feature modules</h2>

Feature modules are NgModules, which are used for the purpose of organizing code. The feature module can be created with Angular CLI using the below command in the root directory,

```javascript
ng generate module MyCustomFeature //
```

Angular CLI creates a folder called `my-custom-feature` with a file inside called `my-custom-feature.module.ts` with the following contents

```javascript
import { NgModule } from '@angular/core';
import { CommonModule } from '@angular/common';

@NgModule({
imports: [
    CommonModule
],
declarations: []
})
export class MyCustomFeature { }
```

**Note:**  The "Module" suffix shouldn't present in the name because the CLI appends it.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the types of feature modules</h2>

Below are the five categories of feature modules,

1. **Domain:** Deliver a user experience dedicated to a particular application domain(For example, place an order, registration etc)
2. **Routed:** These are domain feature modules whose top components are the targets of router navigation routes.
3. **Routing:** It provides routing configuration for another module.
4. **Service:** It provides utility services such as data access and messaging(For example, HttpClientModule)
5. **Widget:** It makes components, directives, and pipes available to external modules(For example, third-party libraries such as Material UI)

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the imported modules in CLI generated feature modules</h2>

In the CLI generated feature module, there are two JavaScript import statements at the top of the file

1. **NgModule:** InOrder to use the `@NgModule` decorator
2. **CommonModule:** It provides many common directives such as `ngIf` and `ngFor`.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the purpose of common module</h2>

The commonly-needed services, pipes, and directives provided by @angular/common module. Apart from these HttpClientModule is available under @angular/common/http.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is Angular Material</h2>

Angular Material is a collection of Material Design components for Angular framework following the Material Design spec. You can apply Material Design very easily using Angular Material. The installation can be done through npm or yarn,

```bash
npm install --save @angular/material @angular/cdk @angular/animations
(OR)
yarn add @angular/material @angular/cdk @angular/animations
```
It supports the most recent two versions of all major browsers. The latest version of Angular material is 8.1.1

**[⬆ Back to Top](#table-of-contents)**

### <h2>What happens if browserModule used in feature module</h2>

If you do import `BrowserModule` into a lazy loaded feature module, Angular returns an error telling you to use `CommonModule` instead. Because BrowserModule’s providers are for the entire app so it should only be in the root module, not in feature module. Whereas Feature modules only need the common directives in CommonModule.

![ScreenShot](images/browser-module-error.gif)

**[⬆ Back to Top](#table-of-contents)**

### <h2>What happens if I import the same module twice</h2>

If multiple modules imports the same module then angular evaluates it only once (When it encounters the module first time). It follows this condition even the module appears at any level in a hierarchy of imported NgModules.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How does forRoot method helpful to avoid duplicate router instances</h2>

If the `RouterModule` module didn’t have forRoot() static method then each feature module would instantiate a new Router instance, which leads to broken application due to duplicate instances. After using forRoot() method, the root application module imports `RouterModule.forRoot(...)` and gets a Router, and all feature modules import `RouterModule.forChild(...)` which does not instantiate another Router.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the differences between ngmodule and javascript module</h2>

Below are the main differences between Angular NgModule and javascript module,

| NgModule                                                                          | JavaScript module                               |
| --------------------------------------------------------------------------------- | ----------------------------------------------- |
| NgModule bounds declarable classes only                                           | There is no restriction classes                 |
| List the module's classes in declarations array only                              | Can define all member classes in one giant file |
| It only export the declarable classes it owns or imports from other modules       | It can export any classes                       |
| Extend the entire application with services by adding providers to provides array | Can't extend the application with services      |

**[⬆ Back to Top](#table-of-contents)**

### <h2>Give few examples for NgModules</h2>

The Angular core libraries and third-party libraries are available as NgModules.

1. Angular libraries such as FormsModule, HttpClientModule, and RouterModule are NgModules.
2. Many third-party libraries such as Material Design, Ionic, and AngularFire2 are NgModules.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is declarable in Angular</h2>

Declarable is a class type that you can add to the declarations list of an NgModule. The class types such as components, directives, and pipes comes can be declared in the module. The structure of declarations would be,

```javascript
declarations: [
    YourComponent,
    YourPipe,
    YourDirective
],
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the restrictions on declarable classes</h2>

Below classes shouldn't be declared,

1. A class that's already declared in another NgModule
2. Ngmodule classes
3. Service classes
4. Helper classes

**[⬆ Back to Top](#table-of-contents)**

### <h2>What classes should not be added to declarations</h2>

The below class types shouldn't be added to declarations

1. A class which is already declared in any another module.
2. Directives imported from another module.
3. Module classes.
4. Service classes.
5. Non-Angular classes and objects, such as strings, numbers, functions, entity models, configurations, business logic, and helper classes.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the possible errors with declarations</h2>

There are two common possible errors with declarations array,

1. If you use a component without declaring it, Angular returns an error message.
2. If you try to declare the same class in more than one module then compiler emits an error.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the steps to use declaration elements</h2>

Below are the steps to be followed to use declaration elements.

1. Create the element(component, directive and pipes) and export it from the file where you wrote it
2. Import it into the appropriate module.
3. Declare it in the @NgModule declarations array.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a provider</h2>

A provider is an instruction to the Dependency Injection system on how to obtain a value for a dependency(aka services created). The service can be provided using Angular CLI as below,

```javascript
ng generate service my-service
```

The created service by CLI would be as below,

```js
import { Injectable } from '@angular/core';

@Injectable({
providedIn: 'root', //Angular provide the service in root injector
})
export class MyService {
}
```
**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the recommendation for provider scope</h2>

You should always provide your service in the root injector unless there is a case where you want the service to be available only if you import a particular @NgModule.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you configure injectors with providers at different levels</h2>

You can configure injectors with providers at different levels of your application by setting a metadata value. The configuration can happen in one of three places,

1. In the `@Injectable()` decorator for the service itself
2. In the `@NgModule()` decorator for an NgModule
3. In the `@Component()` decorator for a component

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you restrict provider scope to a module</h2>

It is possible to restrict service provider scope to a specific module instead making available to entire application. There are two possible ways to do it.

1. **Using providedIn in service:**

```js
import { Injectable } from '@angular/core';
import { SomeModule } from './some.module';

@Injectable({
    providedIn: SomeModule,
})
export class SomeService {
}
```

2. **Declare provider for the service in module:**

```js
import { NgModule } from '@angular/core';

import { SomeService } from './some.service';

@NgModule({
    providers: [SomeService],
})
export class SomeModule {
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is the reason for No provider for HTTP exception</h2>

This exception is due to missing HttpClientModule in your module. You just need to import in module as below,

```javascript
import { HttpClientModule } from '@angular/common/http';

@NgModule({
imports: [
    BrowserModule,
    HttpClientModule,
],
declarations: [ AppComponent ],
bootstrap:    [ AppComponent ]
})
export class AppModule { }
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a bootstrapping module</h2>

Every application has at least one Angular module, the root module that you bootstrap to launch the application is called as bootstrapping module. It is commonly known as `AppModule`. The default structure of `AppModule` generated by AngularCLI would be as follows:

```javascript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { HttpClientModule } from '@angular/common/http';

import { AppComponent } from './app.component';

/* the AppModule class with the @NgModule decorator */
@NgModule({
    declarations: [
    AppComponent
    ],
    imports: [
    BrowserModule,
    FormsModule,
    HttpClientModule
    ],
    providers: [],
    bootstrap: [AppComponent]
})
export class AppModule { }
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a bootstrapped component</h2>

A bootstrapped component is an entry component that Angular loads into the DOM during the bootstrap process or application launch time. Generally, this bootstrapped or root component is named as `AppComponent` in your root module using `bootstrap` property as below.

```js
@NgModule({
declarations: [
    AppComponent
],
imports: [
    BrowserModule,
    FormsModule,
    HttpClientModule,
    AppRoutingModule
],
providers: [],
bootstrap: [AppComponent] // bootstrapped entry component need to be declared here
})
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you manually bootstrap an application</h2>

You can use `ngDoBootstrap` hook for a manual bootstrapping of the application instead of using bootstrap array in `@NgModule` annotation. This hook is part of `DoBootstap` interface.

```js
interface DoBootstrap {
    ngDoBootstrap(appRef: ApplicationRef): void
}
```

The module needs to be implement the above interface to use the hook for bootstrapping.

```js
class AppModule implements DoBootstrap {
    ngDoBootstrap(appRef: ApplicationRef) {
        appRef.bootstrap(AppComponent); // bootstrapped entry component need to be passed
    }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>Is it necessary for bootstrapped component to be entry component</h2>

Yes, the bootstrapped component needs to be an entry component. This is because the bootstrapping process is an imperative process.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Why is not necessary to use entryComponents array every time</h2>

Most of the time, you don't need to explicity to set entry components in entryComponents array of ngModule decorator. Because angular adds components from both @NgModule.bootstrap and route definitions to entry components automatically.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Do I still need to use entryComponents array in Angular9</h2>

No. In previous angular releases, the entryComponents array of ngModule decorator is used to tell the compiler which components would be created and inserted dynamically in the view. In Angular9, this is not required anymore with Ivy.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a routed entry component</h2>

The components referenced in router configuration are called as routed entry components. This routed entry component defined in a route definition as below,

```js
const routes: Routes = [
    {
        path: '',
        component: TodoListComponent // router entry component
    }
];
```
Since router definition requires you to add the component in two places (router and entryComponents), these components are always entry components.

**Note:** The compilers are smart enough to recognize a router definition and automatically add the router component into `entryComponents`.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is an entry component</h2>

An entry component is any component that Angular loads imperatively(i.e, not referencing it in the template) by type. Due to this behavior, they can’t be found by the Angular compiler during compilation. These components created dynamically with `ComponentFactoryResolver`.

Basically, there are two main kinds of entry components which are following -

1. The bootstrapped root component
2. A component you specify in a route

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is a shared module</h2>

The Shared Module is the module in which you put commonly used directives, pipes, and components into one module that is shared(import it) throughout the application.

For example, the below shared module imports CommonModule, FormsModule for common directives and components, pipes and directives based on the need,

```js
import { CommonModule } from '@angular/common';
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { UserComponent } from './user.component';
import { NewUserDirective } from './new-user.directive';
import { OrdersPipe } from './orders.pipe';

@NgModule({
imports:      [ CommonModule ],
declarations: [ UserComponent, NewUserDirective, OrdersPipe ],
exports:      [ UserComponent, NewUserDirective, OrdersPipe,
                CommonModule, FormsModule ]
})
export class SharedModule { }
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>Can I share services using modules</h2>

No, it is not recommended to share services by importing module. i.e Import modules when you want to use directives, pipes, and components only. The best approach to get a hold of shared services is through 'Angular dependency injection' because importing a module will result in a new service instance.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you provide a singleton service</h2>

There are two possible ways to provide a singleton service.

1. Set the providedIn property of the @Injectable() to "root". This is the preferred way(starting from Angular 6.0) of creating a singleton service since it makes your services tree-shakable.

```js
import { Injectable } from '@angular/core';

@Injectable({
    providedIn: 'root',
})
export class MyService {
}
```

2. Include the service in root module or in a module that is only imported by root module. It has been used to register services before Angular 6.0.

```js
@NgModule({
    ...
    providers: [MyService],
    ...
})
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the different ways to remove duplicate service registration</h2>

If a module defines provides and declarations then loading the module in multiple feature modules will duplicate the registration of the service. Below are the different ways to prevent this duplicate behavior.

1. Use the providedIn syntax instead of registering the service in the module.
2. Separate your services into their own module.
3. Define forRoot() and forChild() methods in the module.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Is it mandatory to use injectable on every service class</h2>

No. The `@Injectable()` decorator is not strictly required if the class has other Angular decorators on it or does not have any dependencies. But the important thing here is any class that is going to be injected with Angular is decorated. i.e, If we add the decorator, the metadata `design:paramtypes` is added, and the dependency injection can do it's job. That is the exact reason to add the @Injectable() decorator on a service if this service has some dependencies itself.

For example, Let's see the different variations of AppService in a root component,

1. The below AppService can be injected in AppComponent without any problems. This is because there are no dependency services inside AppService.

```js
export class AppService {
constructor() {
    console.log('A new app service');
}
}
```

2. The below AppService with dummy decorator and httpService can be injected in AppComponent without any problems. This is because meta information is generated with dummy decorator.

```js
function SomeDummyDecorator() {
    return (constructor: Function) => console.log(constructor);
}

@SomeDummyDecorator()
export class AppService {
    constructor(http: HttpService) {
        console.log(http);
    }
}
```

and the generated javascript code of above service has meta information about HttpService,

```js
var AppService = (function () {
    function AppService(http) {
        console.log(http);
    }
    AppService = __decorate([
        core_1.Injectable(),
        __metadata('design:paramtypes', [http_service_1.HttpService])
    ], AppService);
    return AppService;
}());
exports.AppService = AppService;
```

3. The below AppService with @injectable decorator and httpService can be injected in AppComponent without any problems. This is because meta information is generated with Injectable decorator.

```js
@Injectable({
providedIn: 'root',
})
export class AppService {
    constructor(http: HttpService) {
        console.log(http);
    }
}
```
**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the types of injector hierarchies</h2>

There are two types of injector hierarchies in Angular

1. **ModuleInjector hierarchy:** It configure on a module level using an @NgModule() or @Injectable() annotation.
2. **ElementInjector hierarchy:** It created implicitly at each DOM element. Also it is empty by default unless you configure it in the providers property on @Directive() or @Component().

**[⬆ Back to Top](#table-of-contents)**

### <h2>How to inject the dynamic script in angular</h2>

Using DomSanitizer we can inject the dynamic Html,Style,Script,Url.

```ts
import { Component, OnInit } from '@angular/core';
import { DomSanitizer } from '@angular/platform-browser';
@Component({
selector: 'my-app',
template: `
    <div [innerHtml]="htmlSnippet"></div>
`,
})
export class App {
    constructor(protected sanitizer: DomSanitizer) {}
    htmlSnippet: string = this.sanitizer.bypassSecurityTrustScript("<script>safeCode()</script>");
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the differences between AngularJS and Angular with respect to dependency injection</h2>

Dependency injection is a common component in both AngularJS and Angular, but there are some key differences between the two frameworks in how it actually works.

| AngularJS                                                                   | Angular                                                                                                     |
| --------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| Dependency injection tokens are always strings                              | Tokens can have different types. They are often classes and sometimes can be strings.                       |
| There is exactly one injector even though it is a multi-module applications | There is a tree hierarchy of injectors, with a root injector and an additional injector for each component. |

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is HttpClient and its benefits</h2>

Most of the Front-end applications communicate with backend services over `HTTP` protocol using either `XMLHttpRequest` interface or the `fetch()` API. Angular provides a simplified client HTTP API known as `HttpClient` which is based on top of `XMLHttpRequest` interface. This client is available from `@angular/common/http` package.

You can import in your root module as below:

```javascript
import { HttpClientModule } from '@angular/common/http';
```

The major advantages of HttpClient can be listed as below,
1. Contains testability features
2. Provides typed request and response objects
3. Intercept request and response
4. Supports Observalbe APIs
5. Supports streamlined error handling

**[⬆ Back to Top](#table-of-contents)**

### <h2>Explain on how to use HttpClient with an example</h2>

Below are the steps need to be followed for the usage of `HttpClient`.

1. Import `HttpClient` into root module:

```javascript
import { HttpClientModule } from '@angular/common/http';
@NgModule({
imports: [
    BrowserModule,
    // import HttpClientModule after BrowserModule.
    HttpClientModule,
],
......
})
export class AppModule {}
```

2. Inject the `HttpClient` into the application:

Let's create a userProfileService(`userprofile.service.ts`) as an example. It also defines get method of `HttpClient`:

```javascript
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';

const userProfileUrl: string = 'assets/data/profile.json';

@Injectable()
export class UserProfileService {
    constructor(private http: HttpClient) { }

    getUserProfile() {
        return this.http.get(this.userProfileUrl);
    }
}
```

3. Create a component for subscribing service:

Let's create a component called UserProfileComponent(`userprofile.component.ts`), which injects `UserProfileService` and invokes the service method:

```javascript
fetchUserProfile() {
this.userProfileService.getUserProfile()
    .subscribe((data: User) => this.user = {
        id: data['userId'],
        name: data['firstName'],
        city:  data['city']
    });
}
```
Since the above service method returns an Observable which needs to be subscribed in the component.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How can you read full response</h2>

The response body doesn't or may not return full response data because sometimes servers also return special headers or status code, which are important for the application workflow. In order to get the full response, you should use `observe` option from `HttpClient`:

```javascript
getUserResponse(): Observable<HttpResponse<User>> {
    return this.http.get<User>(
    this.userUrl, { observe: 'response' });
}
```
Now `HttpClient.get()` method returns an Observable of typed `HttpResponse` rather than just the `JSON` data.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you perform Error handling</h2>

If the request fails on the server or fails to reach the server due to network issues, then `HttpClient` will return an error object instead of a successful reponse. In this case, you need to handle in the component by passing `error` object as a second callback to `subscribe()` method.

Let's see how it can be handled in the component with an example,

```javascript
fetchUser() {
    this.userService.getProfile()
    .subscribe(
        (data: User) => this.userProfile = { ...data }, // success path
        error => this.error = error // error path
    );
}
```
It is always a good idea to give the user some meaningful feedback instead of displaying the raw error object returned from `HttpClient`.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you pass headers for HTTP client</h2>

You can directly pass object map for http client or create HttpHeaders class to supply the headers.

```javascript
constructor(private _http: HttpClient) {}
this._http.get('someUrl',{
    headers: {'header1':'value1','header2':'value2'}
});

(or)
let headers = new HttpHeaders().set('header1', headerValue1); // create header object
headers = headers.append('header2', headerValue2); // add a new header, creating a new object
headers = headers.append('header3', headerValue3); // add another header

let params = new HttpParams().set('param1', value1); // create params object
params = params.append('param2', value2); // add a new param, creating a new object
params = params.append('param3', value3); // add another param

return this._http.get<any[]>('someUrl', { headers: headers, params: params })
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>Is angular prevents http level vulnerabilities</h2>

Angular has built-in support for preventing http level vulnerabilities such as as cross-site request forgery (CSRF or XSRF) and cross-site script inclusion (XSSI). Even though these vulnerabilities need to be mitigated on server-side, Angular provides helpers to make the integration easier on the client side.

1. HttpClient supports a token mechanism used to prevent XSRF attacks
2. HttpClient library recognizes the convention of prefixed JSON responses(which non-executable js code with ")]}',\\n" characters) and automatically strips the string ")]}',\\n" from all responses before further parsing

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is angular animation</h2>

Angular's animation system is built on CSS functionality in order to animate any property that the browser considers animatable. These properties includes positions, sizes, transforms, colors, borders etc. The Angular modules for animations are **@angular/animations** and **@angular/platform-browser** and these dependencies are automatically added to your project when you create a project using Angular CLI.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the steps to use animation module</h2>

You need to follow below steps to implement animation in your angular project,

1. **Enabling the animations module:** Import BrowserAnimationsModule to add animation capabilities into your Angular root application module(for example, src/app/app.module.ts).

```javascript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';

@NgModule({
    imports: [
    BrowserModule,
    BrowserAnimationsModule
    ],
    declarations: [ ],
    bootstrap: [ ]
})
export class AppModule { }
```

2. **Importing animation functions into component files:** Import required animation functions from @angular/animations in component files(for example, src/app/app.component.ts).

```javascript
import {
    trigger,
    state,
    style,
    animate,
    transition,
    // ...
} from '@angular/animations';
```

3. **Adding the animation metadata property:** add a metadata property called animations: within the @Component() decorator in component files(for example, src/app/app.component.ts)

```javascript
@Component({
    selector: 'app-root',
    templateUrl: 'app.component.html',
    styleUrls: ['app.component.css'],
    animations: [
    // animation triggers go here
    ]
})
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you trigger an animation</h2>

Angular provides a `trigger()` function for animation in order to collect the states and transitions with a specific animation name, so that you can attach it to the triggering element in the HTML template. This function watch for changes and trigger initiates the actions when a change occurs.

For example, let's create trigger named `upDown`, and attach it to the button element.

```js
content_copy
@Component({
selector: 'app-up-down',
animations: [
    trigger('upDown', [
    state('up', style({
        height: '200px',
        opacity: 1,
        backgroundColor: 'yellow'
    })),
    state('down', style({
        height: '100px',
        opacity: 0.5,
        backgroundColor: 'green'
    })),
    transition('up => down', [
        animate('1s')
    ]),
    transition('down => up', [
        animate('0.5s')
    ]),
    ]),
],
templateUrl: 'up-down.component.html',
styleUrls: ['up-down.component.css']
})
export class UpDownComponent {
isUp = true;

toggle() {
    this.isUp = !this.isUp;
}
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

### <h2>What is Angular Ivy</h2>

Angular Ivy is a new rendering engine for Angular. You can choose to opt in a preview version of Ivy from Angular version 8.

1. You can enable ivy in a new project by using the --enable-ivy flag with the ng new command

```bash
ng new ivy-demo-app --enable-ivy
```

2. You can add it to an existing project by adding `enableIvy` option in the `angularCompilerOptions` in your project's `tsconfig.app.json`.

```javascript
{
    "compilerOptions": { ... },
    "angularCompilerOptions": {
    "enableIvy": true
    }
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the features included in ivy preview</h2>

You can expect below features with Ivy preview,

1. Generated code that is easier to read and debug at runtime
2. Faster re-build time
3. Improved payload size
4. Improved template type checking

**[⬆ Back to Top](#table-of-contents)**

### <h2>Can I use AOT compilation with Ivy</h2>

Yes, it is a recommended configuration. Also, AOT compilation with Ivy is faster. So you need set the default build options(with in angular.json) for your project to always use AOT compilation.

```javascript
{
"projects": {
    "my-project": {
    "architect": {
        "build": {
        "options": {
            ...
            "aot": true,
        }
        }
    }
    }
}
}
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is Angular Language Service</h2>

The Angular Language Service is a way to get completions, errors, hints, and navigation inside your Angular templates whether they are external in an HTML file or embedded in annotations/decorators in a string. It has the ability to autodetect that you are opening an Angular file, reads your `tsconfig.json` file, finds all the templates you have in your application, and then provides all the language services.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you install angular language service in the project</h2>

You can install Angular Language Service in your project with the following npm command,

```javascript
npm install --save-dev @angular/language-service
```
After that add the following to the "compilerOptions" section of your project's tsconfig.json

```javascript
"plugins": [
    {"name": "@angular/language-service"}
]
```
**Note:** The completion and diagnostic services works for .ts files only. You need to use custom plugins for supporting HTML files.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Is there any editor support for Angular Language Service</h2>

Yes, Angular Language Service is currently available for Visual Studio Code and WebStorm IDEs. You need to install angular language service using an extension and devDependency respectively. In sublime editor, you need to install typescript which has has a language service plugin model.

**[⬆ Back to Top](#table-of-contents)**

### <h2>Explain the features provided by Angular Language Service</h2>

Basically there are 3 main features provided by Angular Language Service,

1. **Autocompletion:** Autocompletion can speed up your development time by providing you with contextual possibilities and hints as you type with in an interpolation and elements.

     ![ScreenShot](images/language-completion.gif)

2. **Error checking:** It can also warn you of mistakes in your code.

     ![ScreenShot](images/language-error.gif)

3. **Navigation:** Navigation allows you to hover a component, directive, module and then click and press F12 to go directly to its definition.

     ![ScreenShot](images/language-navigation.gif)

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is Bazel tool</h2>

Bazel is a powerful build tool developed and massively used by Google and it can keep track of the dependencies between different packages and build targets. In Angular8, you can build your CLI application with Bazel.

**Note:** The Angular framework itself is built with Bazel.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What are the advantages of Bazel tool</h2>

Below are the list of key advantages of Bazel tool,

1. It creates the possibility of building your back-ends and front-ends with the same tool
2. The incremental build and tests
3. It creates the possibility to have remote builds and cache on a build farm.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you use Bazel with Angular CLI</h2>

The @angular/bazel package provides a builder that allows Angular CLI to use Bazel as the build tool.

1. **Use in an existing applciation:** Add @angular/bazel using CLI

```javascript
ng add @angular/bazel
```

2. **Use in a new application:** Install the package and create the application with collection option

```javascript
npm install -g @angular/bazel
ng new --collection=@angular/bazel
```

When you use ng build and ng serve commands, Bazel is used behind the scenes and outputs the results in dist/bin folder.

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you run Bazel directly</h2>

Sometimes you may want to bypass the Angular CLI builder and run Bazel directly using Bazel CLI. You can install it globally using @bazel/bazel npm package. i.e, Bazel CLI is available under @bazel/bazel package. After you can apply the below common commands,

```ts
bazel build [targets] // Compile the default output artifacts of the given targets.
bazel test [targets] // Run the tests with *_test targets found in the pattern.
bazel run [target]: Compile the program represented by target and then run it.
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is schematic</h2>

It's a scaffolding library that defines how to generate or transform a programming project by creating, modifying, refactoring, or moving files and code. It defines rules that operate on a virtual file system called a tree.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is rule in Schematics</h2>

In schematics world, it's a function that operates on a file tree to create, delete, or modify files in a specific manner.

**[⬆ Back to Top](#table-of-contents)**

### <h2>What is Schematics CLI</h2>

Schematics come with their own command-line tool known as Schematics CLI. It is used to install the schematics executable, which you can use to create a new schematics collection with an initial named schematic. The collection folder is a workspace for schematics. You can also use the schematics command to add a new schematic to an existing collection, or extend an existing schematic. You can install Schematic CLI globally as below,

```bash
npm install -g @angular-devkit/schematics-cli
```

**[⬆ Back to Top](#table-of-contents)**

### <h2>How do you create schematics for libraries</h2>

You can create your own schematic collections to integrate your library with the Angular CLI. These collections are classified as 3 main schematics,

1. **Add schematics:** These schematics are used to install library in an Angular workspace using `ng add` command. For example, @angular/material schematic tells the add command to install and set up Angular Material and theming.

2. **Generate schematics**: These schematics are used to modify projects, add configurations and scripts, and scaffold artifacts in library using `ng generate` command. For example, @angular/material generation schematic supplies generation schematics for the UI components. Let's say the table component is generated using `ng generate @angular/material:table `.

3. **Update schematics:** These schematics are used to update library's dependencies and adjust for breaking changes in a new library release using `ng update` command. For example, @angular/material update schematic updates material and cdk dependencies using `ng update @angular/material` command.

**[⬆ Back to Top](#table-of-contents)**





<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
