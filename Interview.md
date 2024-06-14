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







<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
