<h1>Angular Interview Questions and Answers</h1>

### Table of Contents

| No. | Questions                                                                                                                             |
| --- | ------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is a data binding](#What-is-a-data-binding)                                                                                     |
| 2   | [What is interpolation](#What-is-interpolation)                                                                                       |
| 3   | [How do you categorize data binding types](#How-do-you-categorize-data-binding-types)                                                 |
| 4   | [What is the difference between interpolated content and innerHTM](#What-is-the-difference-between-interpolated-content-and-innerHTM) |
| 4   | [What are lifecycle hooks available](#What-are-lifecycle-hooks-available)                                                             |
| 4   | [What is the difference between constructor and ngOnInit](#What-is-the-difference-between-constructor-and-ngOnInit)                   |
| 4   | [What are the lifecycle hooks of a zone](#What-are-the-lifecycle-hooks-of-a-zone)                                                     |
| 4   | [What are directives](#What-are-directives)                                                                                           |
| 4   | [What are the differences between Component and Directive](#What-are-the-differences-between-Component-and-Directive)                 |
| 4   | [What is the purpose of *ngFor directive](#What-is-the-purpose-of-*ngFor-directive)                                                   |
| 4   | [What is the purpose of *ngIf directive](#What-is-the-purpose-of-*ngIf-directive)                                                     |
| 4   | [What are the various kinds of directives](#What-are-the-various-kinds-of-directives)                                                 |
| 4   | [How do you create directives using CLI](#How-do-you-create-directives-using-CLI)                                                     |
| 4   | [Give an example for attribute directives](#Give-an-example-for-attribute-directives)                                                 |
| 4   | [What is the purpose of hidden property](#What-is-the-purpose-of-hidden-property)                                                     |
| 4   | [What is the difference between ngIf and hidden property](#What-is-the-difference-between-ngIf-and-hidden-property)                   |
| 4   | [What is index property in ngFor directive](#What-is-index-property-in-ngFor-directive)                                               |
| 4   | [What is the purpose of ngFor trackBy](#What-is-the-purpose-of-ngFor-trackBy)                                                         |
| 4   | [What is the purpose of ngSwitch directive](#What-is-the-purpose-of-ngSwitch-directive)                                               |
| 4   | [How to set ngFor and ngIf on the same element](#How-to-set-ngFor-and-ngIf-on-the-same-element)                                       |
| 4   | [What is host property in css](#What-is-host-property-in-css)                                                                         |
| 4   | [What is metadata](#What-is-metadata)                                                                                                 |
| 4   | [What are class field decorators](#What-are-class-field-decorators)                                                                   |
| 4   | [What are the class decorators in Angular](#What-are-the-class-decorators-in-Angular)                                                 |
| 4   | [Is it possible to do aliasing for inputs and outputs](#Is-it-possible-to-do-aliasing-for-inputs-and-outputs)                         |
| 4   | [What are pipes](#What-are-pipes)                                                                                                     |
| 4   | [What is the purpose of async pipe](#What-is-the-purpose-of-async-pipe)                                                               |
| 4   | [What is a parameterized pipe](#What-is-a-parameterized-pipe)                                                                         |
| 4   | [How do you chain pipes](#How-do-you-chain-pipes)                                                                                     |
| 4   | [What is a custom pipe](#What-is-a-custom-pipe)                                                                                       |
| 4   | [Give an example of custom pipe](#Give-an-example-of-custom-pipe)                                                                     |
| 4   | [What is the difference between pure and impure pipe](#What-is-the-difference-between-pure-and-impure-pipe)                           |
| 4   | [What is slice pipe](#What-is-slice-pipe)                                                                                             |
| 4   | [What are the list of template expression operators](#What-are-the-list-of-template-expression-operators)                             |
| 4   | [What is the precedence between pipe and ternary operators](#What-is-the-precedence-between-pipe-and-ternary-operators)               |
| 4   | [How does angular finds components, directives and pipes](#How-does-angular-finds-components,-directives-and-pipes)                   |
| 4   | [What are Http Interceptors](#What-are-Http-Interceptors)                                                                             |
| 4   | [What are the applications of HTTP interceptors](#What-are-the-applications-of-HTTP-interceptors)                                     |
| 4   | [How can I use interceptor for an entire application](#How-can-I-use-interceptor-for-an-entire-application)                           |

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







<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
