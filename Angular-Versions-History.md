<h1>AngularJS 1.X - 2010</h1>

- AngularJS is a free and open-source JavaScript framework that helps developers build modern web applications. It extends HTML with new attributes and it is perfect for single-page applications (SPAs).
- AngularJS, developed by Google, has been important in web development since its inception in 2009. AngularJS excels at building SPAs. These are applications that load in the browser once and update content without needing to refresh the entire page, providing a smoother user experience.
- A single page application is a web application which provide users to a very fast and reactive experience. It contains menu, buttons, and blocks on a single page and when a user clicks any of them, it dynamically rewrites the current page instead of loading new pages from the server. This is the reason behind its robustness.

<h3>Key Features</h3>

1. MVC Architecture - Model-View-Controller (MVC)
2. Two-Way Data Binding
3. Directives
4. Services
5. Dependency Injection

<h1>Angular 2 - 2016</h1>

Angular 2, developed by Google, is a robust and widely popular open-source framework designed to create scalable and interactive web applications. Since its initial release in 2016, Angular 2 has evolved significantly, offering improved features and enhanced usability. Angular is a platform and framework for building single-page client applications using HTML and TypeScript. It is written in TypeScript and makes use of TypeScript libraries for core and optional functionality. Angular 2 has better event-handling capabilities, powerful templates, and better support for mobile devices.

<h3>Key Features</h3>

- **Component-based architecture**: Applications are built using reusable components, which makes them easier to maintain and scale.
- **TypeScript**: Angular 2 uses TypeScript, a superset of JavaScript, which provides static typing and other features that improve code quality and developer experience.
- **Data binding**: Angular 2 uses two-way data binding, which automatically synchronizes data between the model and the view. This simplifies development and reduces the need for manual DOM manipulation.
- **Dependency injection**: Angular 2 uses dependency injection, which makes it easier to test and reuse code.
- **Routing**: Angular 2 has a built-in routing system that makes it easy to navigate between different views in your application.
- **Mobile development**: Angular 2 is well-suited for developing mobile applications, as it produces code that is optimized for performance and can be run on a variety of devices.

<h1>Angular 3</h1>

<h1>Angular 4 - 2017</h1>

Angular 4 was released 5 years after the official release of AngularJS. Between these two versions, Angular 2 was introduced which was a complete re-write of AngularJS. The ‘MVC’ architecture of AngularJS was discarded a new ‘service-controller’ architecture was introduced in Angular 2. After Angular 2 came Angular 4 which was much more efficient than its predecessor. However, the architecture used in both the versions was the same and thus upgrading the project from v2 to v4 was comparatively easier, than upgrading from JS to v2.
Angular 3 was skipped because the router package was already in version 3.3.0. To avoid any further glitches, the team decided to skip v3.x and upgrade all the other modules directly to v4.0. The angular 4 initially release in March 2017.

<h3>Key Features</h3>

- **Architecture**: MVC architecture of AngularJS was replaced by a ‘service-controller’ architecture.
- **View Engine**: The view engine helps in reducing the component code by 60%. This makes the application lightweight as the bundles are reduced in size by several kilobytes.
- **Animation**: Animation now has a separate package. Animation can also be imported from the `BrowserAnimationsModule` from `@angular/platform-browser/animations`.
- **Typescript**: Angular 4 uses Typescript v2.2. Typescript is considered to be the superset of Javascript.
- **New Keywords**: Some new keywords like ‘as’ was introduced. This is generally used to store the output of a slice or a command in some variable. The ‘else’ condition was also introduced in Angular 4. The introduction of the ‘if-else; looping condition helped in code condensation.

**Use of ‘as’ keyword**
```html
<div *ngFor="let j of weeks | slice:0:5 as num">
    Months: {{j}} Num: {{num.length}}
</div>
```
**Use of ‘if-else’ condition in Angular 4**
```html
<span *ngIf="isavailable; else condition1">
    Valid Condition.
</span>
<ng-template #condition1>
    Invalid Condition
</ng-template
```
- **Mobile Support**: Angular 4 is supported by almost every modern day mobile browser.
- HTTP Search Parameter: There is no need to call the URLSearchParams for the HTTP search parameter.
- Compatibility with the previous version: Angular 4 is compatible with Angular 2 and AngularJS. Projects developed in Angular 2 will work without any problem in Angular 4.

<h1>Angular 5 - 01 November 2017</h1>

In this article, we will see What’s New and Improved in Angular 5. Angular 5 was released in November 2017, bringing a range of new features and improvements to the popular front-end framework. Let’s take a closer look at some of the most notable changes in this version:

<h3>Key Features</h3>

- **Ivy Renderer**: The most significant change in Angular 5 is the introduction of the Ivy renderer. This new rendering engine is designed to improve the performance and size of Angular applications. Ivy is also more compatible with modern web standards and is expected to make it easier to develop components and libraries. With the introduction of Ivy, developers can expect smaller bundle sizes, faster compilation times, and improved debugging and error messages. Ivy also provides better support for lazy loading and server-side rendering.
- **Improved Compiler**: In addition to Ivy, Angular 5 includes several improvements to the compiler. The compiler is responsible for converting Angular code into JavaScript that can be executed by a browser. The new compiler offers faster compilation times and better error messages. It also supports Ahead-of-Time (AOT) compilation, which can improve the performance of Angular applications.
- **HttpClient**: Angular 5 introduces a new HttpClient module, which is a simplified version of the previous Http module. The new module is designed to be more straightforward to use and more efficient. The HttpClient module provides a more streamlined API for making HTTP requests, as well as improved error handling and interceptors. It also supports progress events, which can be used to track the progress of long-running HTTP requests.
- **Improved Accessibility**: Accessibility (a11y) is an essential consideration for modern web applications, and Angular 5 includes several improvements in this area. The framework now includes better support for screen readers, keyboard navigation, and focus management.
- **Support for Angular Universal State Transfer API and DOM**: Angular Universal is a server-side rendering solution for Angular applications. With Angular 5.0, the framework now supports Angular Universal State Transfer API and DOM. This means that developers can now easily transfer the application state from the server to the client, leading to faster load times and a better user experience.
- **Build Optimizer**: Another major improvement in Angular 5.0 is the introduction of the Build Optimizer. The Build Optimizer is a tool that automatically removes unnecessary code from the application during the build process, leading to smaller bundle sizes and faster load times.
- **Support for Improved Decorator**: In Angular 5.0, the framework introduces an improved version of the @Directive decorator. The new decorator allows developers to define a component as a directive, making it easier to reuse code across different components.
- **ReflectiveInjector with StaticInjector Replacement**: Angular 5.0 replaces ReflectiveInjector with StaticInjector, leading to faster bootstrapping times and improved performance. The new StaticInjector is faster and more efficient than the previous version, making it a significant improvement for Angular developers.
- **Internationalized Number, Date, and Currency Pipes**: Angular 5.0 now supports internationalized pipes for numbers, dates, and currencies. The new pipes make it easier to format and display data in different locales, making Angular applications more accessible to a global audience.
-**Angular Forms adds updateOn Blur Or Submit**: Angular Forms now allows developers to set the updateOn property to either blur or submit. This means that developers can choose when the form updates, leading to a better user experience and improved performance.
- **New Router Lifecycle Events**: Angular 5.0 introduces several new lifecycle events for the router. These new events allow developers to react to changes in the router, leading to more robust and flexible applications.
- **Updates in RxJS 5.5**: Finally, Angular 5.0 comes with updates to RxJS 5.5. The new version of RxJS introduces several new features, including improved performance and new operators. These updates make it easier for developers to work with observables and reactive programming in Angular applications.
- **Other Changes**: In addition to the changes mentioned above, Angular 5 includes several other updates and improvements. Some of the notable changes include:
    - Support for TypeScript 2.4 and 2.5
    - Better support for internationalization (i18n)
    - Improved documentation and examples


In conclusion, Angular 5 introduces several significant improvements to the framework, including the new Ivy renderer, improved compiler, and HttpClient module. The framework also includes several improvements to accessibility and internationalization. From improved performance to new features in RxJS, Angular 5.0 is a significant update for the Angular framework. With these improvements, developers can build faster, more efficient, and more accessible applications than ever before.

<h1>Angular 6 - April 2018</h1>

In this article, we will see What’s New and Improved in Angular 6.0. Angular 6.0 was released in May 2018, bringing a range of new features and improvements to the popular front-end framework. Let’s take a closer look at some of the most notable changes in this version.

<h3>Key Features</h3>

- **RxJS 6**: Angular 6.0 comes with an updated version of RxJS, a library for reactive programming. RxJS 6 introduces several new features and improvements, including better performance, simplified imports, and improved error handling. One of the most significant changes in RxJS 6 is the introduction of “pipeable operators.” This new syntax makes it easier to compose operators and avoid nested subscriptions, improving the readability and maintainability of reactive code.
- **Angular Elements**: Angular 6.0 introduces a new feature called Angular Elements, which allows developers to create custom elements using Angular components. Custom elements are a web standard that allows you to create reusable, encapsulated components that can be used across different frameworks and platforms. Angular Elements makes it easier to create custom elements by providing a simple API for creating and configuring them. It also includes a polyfill that enables custom elements to work in older browsers.
- **Improved Angular CLI**: The Angular CLI (Command Line Interface) has been updated in Angular 6.0 with several improvements. The most notable of these is the ability to generate code for Angular Elements. This makes it easier to create and use custom elements in your Angular applications. Other CLI improvements in Angular 6.0 include better support for libraries, improved error handling, and the ability to configure proxy settings for development servers.
- **Angular Material**: Angular 6.0 includes an updated version of Angular Material, a UI component library for Angular. Angular Material 6 includes several new components, including Tree and Drag-and-Drop, as well as improvements to existing components. Angular Material 6 also includes better support for internationalization (i18n) and improved accessibility (a11y) features.
- **Use ng-template instead of template directive**: One of the major changes in Angular 6.0 is the introduction of ng-template. This new directive can be used instead of the older template directive, which has been deprecated. ng-template is a powerful tool for creating reusable templates that can be used across multiple components. It also provides better performance and improved code organization.
- **Declaring the providers inside the service itself**: Angular 6.0 also introduces a new way to declare providers for services. Instead of declaring providers in the module file, providers can now be declared inside the service itself. This helps to simplify the code and makes it easier to manage dependencies.
- **Use of ng add, ng update**: Angular 6.0 comes with new commands for managing dependencies. The ng add command allows developers to easily add new features and libraries to their application, while the ng update command simplifies the process of updating existing dependencies. These commands make it easier to keep your application up-to-date and take advantage of the latest features and improvements.
- **Multiple Validators for Form Builder Array**: Angular 6.0 introduces a new feature for form builders. Developers can now add multiple validators to form builder arrays, making it easier to validate user input and improve the accuracy of the data collected. This feature is particularly useful for applications that rely heavily on user input, such as e-commerce sites or social media platforms.
- **Other Changes**: In addition to the changes mentioned above, Angular 6.0 includes several other updates and improvements. Some of the notable changes include:
    1. Support for TypeScript 2.7 and 2.8
    2. mproved performance and reduced bundle sizes
    3. Better support for animations and transitions

Angular 6.0 introduces several significant improvements to the framework, including the new Angular Elements feature, updates to RxJS and Angular Material, and improvements to the Angular CLI. The framework also includes several smaller updates and improvements that help to improve performance, reduce bundle sizes, and improve developer productivity. With the introduction of ng-template, simplified service providers, new dependency management commands, and improved form builders, developers can create faster and more reliable applications than ever before.

<h1>Angular 7 - October 2018</h1>

Angular 7 is a TypeScript based front-end web framework by Google. It enables you to create Single Page Applications(SPA) with the help of the concept of components. The components in Angular 7 are structured like a tree i.e. there are parent and child components in which each child component is connected to its respective parent component.

<h3>Key Features</h3>

- **Supports most of the languages**: Angular can be used as a front-end web development tool for the programming languages like Node.js, .Net, PHP, Java Struts, Spring and other servers for real time rendering in just HTML and CSS. It also optimizes the website for better SEO.
- **Code optimization**: It makes the templates in optimized way for today’s JavaScript virtual machines which gives the benefits of hand-written code.
- **Code splitting**: Angular apps are fast and load quickly with the new Component Router (handles routing), which delivers automatic code-splitting and the user only loads the code required to render the view they want.
- **Supports multiple platforms:**
    - `Desktop apps`: It allows you to create desktop installed apps on different operating systems i.e. Windows, Mac or Linux by using the same methods which we use for creating web and native apps.
    - `Progressive web applications`: Progressive web applications are the most common apps which are built with Angular. It provides modern web platform capabilities to deliver high performance installation apps.
- **Productive:**
  - `Templates`: Provides with simple and smooth UI view with intelligent IDE.
  - `Angular CLI`: Angular CLI provides command line tools start building fast, add components and tests, and then instantly deploy.
- **Full Development:**
    - `Testing`: Provides with strong unit testing i.e. it provides Karma and Jasmine for unit testing. By using it, you can check your broken things every time you save.
    - `Accessibility`: In it, you can create accessible applications with ARIA-enabled components, developer guides, and built-in ally test infrastructure.

<h1>Angular 8 - March/April 2019</h1>

<h1>Angular 9 - 06 Feb 2020</h1>

<h1>Angular 10 - 24 Jun 2020</h1>

<h1>Angular 11 - 11 November 2020</h1>

<h1>Angular 12 - 13 May 2021</h1>

<h1>Angular 13 - 03 Nov 2021</h1>

<h1>Angular 14 - 02 Jun 2022</h1>

<h1>Angular 15 - 16 Nov 2022</h1>

<h1>Angular 16 - 03 May 2023</h1>

<h1>Angular 17 - 08 Nov 2023</h1>

<h1>Angular 18 - 22 May 2024</h1>

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
