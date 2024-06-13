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
    - Support for TypeScript 2.7 and 2.8
    - mproved performance and reduced bundle sizes
    - Better support for animations and transitions

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

- **Lazy-loaded modules**: Lazy loading is based on the concepts of Angular Routing and it helps bring down the size of enormous files by lazily loading the data that are required. It uses standard dynamic import syntax instead of a custom string for lazy-loaded modules. This improvement will boost support from the editors VSCode and WebStorm, who would be able to evaluate and validate the imports. Likewise, TypeScript and linters will have the option to distinguish missing or incorrectly spelled modules better.
- **TypeScript 3.4**: Angular 8 supports TypeScript 3.4 and it is required to run Angular 8 project.This update of dependencies on the tool is an approach to synchronize it with the existing ecosystem. It has the most noteworthy advantages with regards to creating clean, decipherable JavaScript codes.
- **Differential Loading by Default**: Differential loading in Angular 8.0 is the prime performance improvement in the update. Differential loading is where browsers will select streamlined or inheritance bundles as indicated by their capabilities and load the correct one automatically. Additionally, clients will receive the bundle they require. In Angular 8.0, the ng build command with the –prod extension does the entire bundling. The bundle size for modern browsers reduces by 7 to 20%.
- **Web Workers**: Web workers are incorporated while constructing the production bundles which are fundamental in improving the parallelizability and helps increase the performance. Angular 8.0 thus adds building support to CLI which provides one bundle for every web worker.
- **Ivy Rendering Engine**: Ivy is included in Angular 8.0 only as an opt-in preview for testing. Angular developers can give it a shot to decide the potential and execution of their Angular application.
    - `Tree shakable`:Unused code is removed so application concentrates on the code it is using.
    - `Local`:Only the components that change are recompiled. This results in quicker compiling.
- Bazel Support: Bazel provides possibility to build CLI application more efficiently and quickly .The benefit of using bazel is the incremental steady form and tests. It provides an opportunity to make the backends and frontends with an equivalent device. It has a likelihood to have remote builds and reserve on the build farm.
- **Opt-In Usage Sharing**: Opt-in sharing telemetry can collect data commands used and the fabricate speed if the user permits them, which will assist developers to improve later on. With this, the open-source web application framework will collect anonymous data only when permitted to do.
- **Router Backward Compatibility**:In Angular 8.0, backward compatibility mode is added to Angular router that assists in creating the way for large projects and make it easier to move to Angular with lazy loading.
- **CLI Workflow Improvements**: The new Builder APIs will take advantage of ng construct, ng test, and ng run a lot of like Schematics gives tap access to ng new, ng create, ng-include and ng update. The Angular CLI is consistently improving, and now the ng-build, ng-test, and ng-run are equipped to be extended by 3rd party libraries and tools. Angular 8.0 comes with a new API that makes modifying and perusing the document much less complex.

<h1>Angular 9 - 06 Feb 2020</h1>

- **Ivy Renderer (Default)**: Angular 9.0 includes the new Ivy renderer as the default rendering engine. Ivy is a new rendering engine that is designed to improve the performance and size of Angular applications. It is also more compatible with modern web standards and is expected to make it easier to develop components and libraries. With the introduction of Ivy, developers can expect smaller bundle sizes, faster compilation times, and improved debugging and error messages. Ivy also provides better support for lazy loading and server-side rendering.
- **Improved Build Size and Performance**: Angular 9.0 includes several improvements to build size and performance. This version introduces a new “ngcc” (Angular Compatibility Compiler) tool that optimizes the size of third-party libraries used in Angular applications. The new “ngcc” tool allows developers to use libraries that were built with previous versions of Angular, without the need to rebuild them. This can significantly reduce the size of the final bundle and improve the performance of the application.
- **Improved Testing and Debugging**: Angular 9.0 includes several improvements to testing and debugging. This version introduces a new “ng test” command that allows developers to run tests in parallel, making the testing process faster and more efficient. Angular 9.0 also includes improvements to the Angular Language Service, which provides better support for intelligent code completion, diagnostics, and navigation in IDEs like Visual Studio Code.
- **Improved Internationalization (i18n)**: Angular 9.0 introduces several improvements to internationalization (i18n). This version includes a new “i18nLocalize” function that makes it easier to translate dynamic content in an Angular application. The new “i18nLocalize” function allows developers to translate content that is generated dynamically, like dates and numbers. This can significantly simplify the process of translating an Angular application and improve the experience for users in different locales.
- **CSS class and style binding improvement**: One of the major changes in Angular 9.0 is the improvement of CSS class and style binding. With the new ngClass and ngStyle directives, developers can now bind CSS classes and styles more easily and efficiently than ever before. This feature makes it easier to manage styles and improves the performance of the application.
- **Build errors and type checking enhancement**: Angular 9.0 also brings significant improvements to build errors and type checking. With the new TypeScript 3.7 support, developers can now enjoy faster and more accurate type checking. This helps to prevent errors and makes it easier to catch bugs early in the development process.
- **Enabling Ahead-of-Time compiler and Improved build times**: Another major improvement in Angular 9.0 is the enabling of the Ahead-of-Time (AOT) compiler by default. This improves the performance of the application and reduces load times by precompiling the application code. Additionally, Angular 9.0 introduces improved build times, making it faster and more efficient to build and deploy applications.
- **New options for ‘providedIn’**: Angular 9.0 introduces new options for the ‘providedIn’ property, making it easier to manage dependencies. With the new ‘any’ option, developers can specify that a service can be provided at any level of the application, allowing for greater flexibility and control.
- **Enhancements in Angular Components**: Finally, Angular 9.0 brings significant enhancements to Angular components. With improved rendering performance and the ability to create dynamic components more easily, developers can create more powerful and flexible user interfaces. Additionally, Angular 9.0 introduces improved support for custom elements, making it easier to integrate Angular components with other web technologies.
- **Other Changes**: In addition to the changes mentioned above, Angular 9.0 includes several other updates and improvements. Some of the notable changes include:
    - Improved support for lazy loading and differential loading
    - Better support for TypeScript 3.7 and 3.8
    - Improved accessibility (a11y) features

<h1>Angular 10 - 24 Jun 2020</h1>

- **Improved Angular CLI**: Angular 10.0 includes improvements to the Angular CLI (Command Line Interface), which is used to generate and manage Angular projects. The new version of the CLI includes several new commands, such as “ng deploy”, which simplifies the process of deploying Angular applications to the web. The Angular CLI also includes improvements to the way it generates code, making it easier to create new components, services, and modules. The CLI now generates TypeScript files instead of JavaScript files by default, which provides better type safety and improves the developer experience.
- **Support for TypeScript 3.9**: Angular 10.0 adds support for TypeScript 3.9, which includes several new features and improvements. The new version of TypeScript introduces support for conditional types, which makes it easier to create complex type relationships in your code. TypeScript 3.9 also includes improvements to the way it handles inference for types, which can improve the developer experience and reduce the number of errors in your code.
- **Improved Angular Material**: Angular 10.0 includes several improvements to Angular Material, which is a set of UI components for Angular applications. The new version of Angular Material includes a range of new components, such as a new date range picker and a new stepper component. Angular Material also includes improvements to accessibility (a11y) and internationalization (i18n), making it easier to create applications that are accessible to a wider range of users.
- **Improved Performance**: Angular 10.0 includes several improvements to performance, making Angular applications faster and more efficient. This version includes a new “global optimization” feature that optimizes the generated code for the entire application, reducing the size of the final bundle and improving performance. The new version of Angular also includes improvements to the way it handles change detection, which can improve the performance of large and complex applications.
- **Changes and Deprecations in Version 10**: One of the significant changes in Angular 10.0 is the introduction of stricter type-checking. This feature ensures that you’re using the right types and reduces the chances of errors in your code. It also makes it easier to maintain and refactor your codebase. Another change is the removal of support for Internet Explorer 9, 10, and IE mobile. This means that Angular 10.0 only supports IE 11 and above. If you’re still using older versions of Internet Explorer, you’ll need to update your browser to use Angular 10.0. In terms of deprecations, Angular 10.0 has removed support for the ViewEngine renderer. The Ivy renderer is now the default and the only supported renderer. If you’re still using ViewEngine, you’ll need to update your code to use Ivy.
- **Ivy Features and Compatibility**: Ivy is a new rendering engine that was introduced in Angular version 9. It’s designed to improve the performance, bundle size, and development experience of Angular applications. In Angular 10.0, Ivy comes with some new features and improvements. One of the most significant changes is the ability to use lazy loading with dynamic imports. This feature can significantly improve the performance of your application, especially if you have a lot of components. Another feature is improved support for internationalization (i18n). Ivy now supports differential loading of i18n translations, which can help reduce the size of your application. If you’re upgrading from an older version of Angular, you might be wondering about Ivy compatibility. The good news is that most third-party libraries are already compatible with Ivy. However, if you’re using a library that’s not compatible, you’ll need to update it or find an alternative.
- **CommonJS Imports**: Another significant change in Angular 10.0 is the introduction of support for CommonJS imports. CommonJS is a module system that’s used in Node.js, and it’s often used in server-side applications. With the new CommonJS imports feature, you can now use modules from Node.js in your Angular application without having to use a bundler like Webpack. This can simplify your build process and make it easier to work with server-side modules.
- **New Default Browser Configuration**: Finally, Angular 10.0 comes with a new default browser configuration. The new configuration disables some of the older and less secure features of the browser, such as a document.write() and synchronous XHR requests. This change can help improve the security and performance of your application, but it might also affect some of your existing code. If you’re using any of the features that have been disabled, you’ll need to update your code to use alternative approaches.
- **Other Changes**: In addition to the changes mentioned above, Angular 10.0 includes several other updates and improvements. Some of the notable changes include:
    - Improved support for lazy loading and differential loading
    - Improved debugging experience with better error messages and stack traces
    - Improved support for Angular Universal, which allows you to generate server-side rendered pages for Angular applications

<h1>Angular 11 - 11 November 2020</h1>

- **Fonts Download Automatically**: Angular import font by default. During integration, Angular CLI will download in-line fonts and connect the appliance. Angular automatically provides this with version 11. You simply got to update your app.
- **Harness Exploration Election**: Angular v9 introduces Item equipment. Provides a strong and readable API to help with the testing of Angular Material objects. This provides developers with how to speak with Angular Material objects employing a supported API during testing.
- **Login and reporting improved**: The Angular developer has made changes to the builder class, reporting is more useful during development. In angular, version 11 reports and logs are easy to read.
- **Renewal of Language Service Review**: The current Angular version of the language service is predicated on View Engine and today they provide an Ivy-based language service. Now, the language service is going to be ready to properly install common types like TypeScript integrator.
- **Updated Hot Module Replacement (HMR) Support**: In version 11 angular developers reviewed CLI to permit HMR when launching an application with ng serve like, `ng serve --hmr`
- After this command the server starts and therefore the console will also report that HMR is running:
- **How to upgrade to Angular version 11:** `ng update @ angular/cli @ angular/core`

<h1>Angular 12 - 13 May 2021</h1>

- **Performance Improvements**: One of the major focuses of Angular 12 is to improve performance. Angular 12 comes with a new compiler that reduces the size of generated code, leading to faster application startup times. The new compiler also supports the latest version of TypeScript, providing better performance and error checking.
- **Improved Webpack 5 Support**: Angular 12 now supports Webpack 5, which comes with several performance improvements and features such as caching, faster builds, and tree shaking. This enables developers to build faster and more efficient applications.
- **Angular Material Updates**: Angular Material is a UI component library for Angular applications. Angular 12 comes with updates to Angular Material, including new components, improved accessibility, and better theming options.
- **Improved Testing Support**: Angular 12 comes with improved testing support, including better mocking of dependencies, improved testing performance, and better error messages.
- **Strict Mode by Default**: A Strict mode is a compiler option that enforces strict type checking and helps catch common errors during development. In Angular 12, strict mode is enabled by default, making it easier for developers to write more reliable and maintainable code.
- **Router Scrolling Improvements**: Angular 12 comes with router scrolling improvements that make it easier to handle scrolling behavior when navigating between pages. The new router scrolling behavior is smoother and more reliable, making for a better user experience.
- **Automatic Font Inlining**: In previous versions of Angular, developers had to manually inline fonts in their applications. With Angular 12, font inlining is now automatic, leading to faster load times and improved performance.
- **Angular Language Service Improvements**: The Angular Language Service is a set of tools that provide code completion, error checking, and other helpful features for Angular developers using Visual Studio Code or other code editors. Angular 12 comes with improvements to the Angular Language Service, making it easier for developers to write code and catch errors before runtime.
- **TypeScript 4.2 Support**: Angular 12 supports TypeScript 4.2, & generally, it is recommended to use the latest version of TypeScript for improved performance and better language features. Angular 12 comes with several new features and improvements, including improved performance, stricter checks, and better error messaging in TypeScript version 4.2. This enhances the development experience and makes it easier for developers to write reliable and maintainable code.
- **Better Error Handling**: Angular 12 comes with better error handling, including more descriptive error messages and improved stack traces. This makes it easier for developers to debug and troubleshoot issues during development and in production.
- **Deprecation of Internet Explorer 11 Support**: Internet Explorer 11 is an outdated browser that does not support modern web standards. In Angular 12, support for Internet Explorer 11 is deprecated, meaning that future versions of Angular will no longer support this browser. This enables developers to use modern web technologies and focus on building for the future.
- **Angular Ivy Concept**: Angular Ivy is the new rendering engine introduced in Angular 9. It is a complete rewrite of the old rendering engine and is designed to make the Angular framework faster, smaller, and more flexible. Some benefits of Ivy include improved performance, smaller bundle sizes, improved debugging, and better compatibility with third-party libraries. Ivy is enabled by default in Angular 12.
- **Transitioning from Legacy i18n Message IDs**: Angular’s i18n feature is used for internationalizing an Angular application. In previous versions of Angular, the i18n message IDs were generated automatically based on the text content of the element. In Angular 12, it is recommended to use a custom message ID instead of the automatically generated IDs. This allows for better stability of the message IDs and prevents unnecessary updates of translations when the text content changes.
- **Angular Protractor**: Angular Protractor is an end-to-end testing framework for Angular applications. It is built on top of WebDriverJS and is designed to make it easy to write and run automated tests for Angular applications. Protractor is included in the Angular CLI and can be used to run tests locally or on a remote server.
- **Nullish Coalescing Operator**: The Nullish coalescing operator (??) is a new operator introduced in TypeScript 3.7. It allows for a concise way to check if a value is null or undefined and provides a default value in case it is. This operator is now supported in Angular 12.
- **Stylish Improvements**: Angular 12 introduces several improvements to the styling of Angular applications. One of the key improvements is the ability to use global styles and style preprocessor files (such as Sass) directly in the Angular CLI without having to manually configure them. This makes it easier to style Angular applications and ensures consistency across the application.

<h1>Angular 13 - 03 Nov 2021</h1>

- **Ivy Improvements**: Angular 13 introduces several Ivy improvements, including better diagnostics, improved AOT (Ahead of Time) compilation, and better tree shaking. Ivy is the new rendering engine in Angular that provides improved performance, smaller bundle sizes, and better error messages. For instance, you can now use dynamic imports with Ivy like this:
```ts
import("./my-component").then(module => {
    // use the component here
});
```
- **Strict Mode**: Angular 13 introduces a new strict mode that enforces strict type checking, improves error messages, and helps catch common mistakes. This can help developers write more reliable and maintainable code.
- Updated Dependencies: Angular 13 updates its dependencies, including TypeScript 4.5, RxJS 7, and Zone.js 0.11. This provides developers with the latest features and improvements in these libraries. For instance, you might be able to use the new “never” type to indicate a function that never returns:
```ts
function handleError(): never {
    throw new Error("Something went wrong");
}
```
- **Angular Material Updates**: Angular Material is a UI component library for Angular that provides a set of pre-built UI components. Angular 13 introduces several updates to Angular Material, including new typography options, improved theming capabilities, and accessibility improvements.
- **Improved Router Performance**: Angular 13 introduces several improvements to the router’s performance, including better support for preloading, improved route reuse strategy, and better query parameter handling. This can help improve the overall performance of Angular applications.
- **Improved DevTools Support & Testing Support**: Angular 13 introduces several improvements to the Angular DevTools, including better support for debugging change detection, improved performance profiling, and better support for testing. On another hand, in Testing Support, Angular 13 includes better support for TestBed, improved error messages, and improved test coverage reporting. This can help developers write more comprehensive and effective tests for their applications.
- **Improved Localization Support**: Angular 13 introduces several improvements to localization support, including better support for date and time formatting, better support for pluralization, and better support for ICU expressions. This can help developers build applications that can support multiple languages and regions.
- **Improved Accessibility**: Angular 13 introduces several accessibility improvements, including better support for aria-label and aria-labelledby attributes, better support for keyboard navigation, and better support for screen readers. This can help developers build more accessible applications that can be used by all users, including those with disabilities. For example, you might be able to use the aria-label attribute like this:
```html
<button aria-label="Submit">Submit</button>
```
- **Faster recompilation**: The Angular team is working on making recompilation faster, particularly for large projects with many components. For example, changes to a component’s HTML template might now take only a few seconds to update, rather than tens of seconds or even minutes.
- **Improved error messages**: The error messages in Angular 13 are expected to be clearer and more informative, making it easier for developers to troubleshoot issues. For example, instead of a cryptic error like “TypeError: Cannot read property ‘foo’ of undefined”, you might see a message like “Error: Could not find data for user ID 123”.
- **Better support for Webpack 5**: Angular 13 is expected to have better compatibility with Webpack 5, which should improve build times and overall performance.
- **Support for TypeScript 4.5**: Angular 13 supports the latest version of TypeScript, which includes several new features and improvements. For example, you can now use recursive type aliases like this:
```ts
type JSONValue = string | number | boolean | null | JSONArray | JSONObject;
type JSONArray = JSONValue[];
type JSONObject = { [key: string]: JSONValue; };
```
- **Angular Package Format (APF)**: The Angular Package Format (APF) is a new feature introduced in Angular v13 that allows developers to create and distribute libraries in a new format that reduces the size of the final bundle by removing unnecessary code. With APF, developers can create packages that contain only the necessary code to run their libraries, resulting in faster loading times for applications that use these libraries.
- **RxJS, TypeScript & Node.js versions supported**: Angular v13 supports RxJS version 7, TypeScript version 4.4, and Node.js version 14 or later. These updated versions bring new features and improvements to the framework, including faster build times and improved performance.
- **Changes made to the Router**: Angular v13 includes several changes to the Router module, including improved support for lazy loading and better handling of route changes. These changes improve the performance and usability of the Router module, making it easier for developers to create complex routing configurations.
- **Enhancements in Angular CLI & Angular testing**: Angular v13 introduces several enhancements to the Angular CLI, including new commands for generating components and services, improved support for building and deploying applications, and better integration with third-party tools. Additionally, the framework now supports faster and more reliable testing, with improvements to the TestBed API and the addition of new testing utilities.
- **Dynamic Components creation**: Finally, Angular v13 includes new features for creating and managing dynamic components. Developers can now create and load components dynamically at runtime, giving them more flexibility in building complex UIs.

<h1>Angular 14 - 02 Jun 2022</h1>

<h3>1. Standalone components, directives, and pipes</h3>

- In Angular 14, you can create a module-less Angular application using the standalone flag. Right now, this feature is in the developer preview state.
- In Angular 13 and older, the NgModule contained component configurations like imports, declarations, pipes, and directives, so there was a need to add NgModule as a separate file. However, in Angular 14, you can create standalone components without NgModule.
- To enable creating a standalone component, you must add the standalone flag (standalone: true) inside the @component decorator and add all the configurations inside the decorator. The root component should be passed as an argument to the bootstrapApplication function provided by @angular/platform-browsers.
```ts
import { Component } from '@angular/core';
import { CommonModule } from '@angular/common';
import { bootstrapApplication } from '@angular/platform-browser';
@Component({
    selector: 'app-root',
    standalone: true,
    imports: [
        // import standalone Components, Directives, and Pipes
        CommonModule // and NgModules
    ],
    template: `
        <div>{{name}}</div>
})
export class SampleComponent {
    name = "Angular 14";
}
// Bootstrap a new Angular application using our `SampleComponent` as a root component.
bootstrapApplication(SampleComponent);
```

<h3>2. Typed Angular forms</h2>

- Typed forms ensure that the values inside form controls, groups, and arrays are type-safe across the entire API surface. This enables safer forms, especially for deeply nested complex cases. The schematic ng update provides backward compatibility for your existing forms. Syncfusion’s Angular Forms components are compatible with the typed Angular forms functionality.
```ts
export class SampleComponent {
    var contactForm = new FormGroup({
     name: new FormControl<string>('', { nonNullable: true }),
     email: new FormControl<string>('', { nonNullable: true }),
     contactNumber: new FormControl<number>(0, { nonNullable: false })
    });
}
```

<h3>3. Streamlined page title accessibility</h3>

- In Angular 14, we can add the router title without any additional import on the page. Refer to the following code example.
```ts
const routes: Routes = [
    {
        path: 'home',
        component: HomeComponent
        title: 'Home page'  // <-- Page title
    },
    {
        path: 'about',
        component: AboutComponent,
        title: 'About page'  // <-- Page title
    }
];
```

<h3>4. Extended developer diagnostics</h3>

- The extendable developer diagnostics feature provides extendable frameworks that help developers better understand the templates and display suggestions for potential enhancements. It helps improve caching before runtime, provide actionable suggestions for a template, and helps diagnose warnings at compile time.

<h3>5. More built-in improvements</h3>

- Angular 14 also includes support for the latest TypeScript 4.7 release and now targets ES2020 by default, which allows the CLI to ship smaller code without paring down features.

<h3>6. Bind to protected component members</h3>

- Now you can bind protected component members directly from the template. Refer to the following code example.

```ts
@Component({
    selector: 'app-root',
    template: '{{ title }}',  // Now compiles!
})
export class SampleComponent {
    protected title: string = 'Angular 14';
}
```
- This feature provides more control over the public API surface of your reusable components.

<h3>7. Optional injectors in embedded Views</h3>

- Angular 14 supports passing in an optional injector when creating an embedded view through ViewContainerRef.createEmbeddedView and TemplateRef.createEmbeddedView. This injector enables customization of dependency injection behavior within the specific template.

```ts
viewContainer.createEmbeddedView(templateRef, context, {
    injector: injector,
})
```

<h3>How to upgrade to Angular 14</h3>

- If you are using Angular 13, run the command `ng update @angular/core@14 @angular/cli@14` to update all Angular dependencies to Angular 14. Also, Angular 14 requires some new prerequisites to build an application.
- Angular 14 prerequisites
  - Typescript 4.7.
  - Node version 14.15.0 or later.

<h1>Angular 15 - 16 Nov 2022</h1>

<h1>Angular 16 - 03 May 2023</h1>

<h1>Angular 17 - 08 Nov 2023</h1>

<h1>Angular 18 - 22 May 2024</h1>

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
