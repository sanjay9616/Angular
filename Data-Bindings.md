<h1>Data Bindings in Angular</h1>

Angular provides three categories of data binding according to the direction of data flow:

<h2>1. From source to view</h2>

```ts
value: string = 'From source to view data binding';
```
```html
<h1>{{value}}</h1>
```

<h2>2. From view to source</h2>

```html
<input type="text" (input)="onInputChange($event)">
```
```ts
value: string = ''
onInputChange(value: string) {
    this.value = value
}
```

<h2>3. In a two-way sequence of view to source to view</h2>

Two-way data binding gives you a way to share data between view to source and vice versa simultaneously.Two-way data binding is a combination of property binding "[]" and event binding "()" and its syntax is called banana in a box syntax [( )].

```html
<input [ngModel]="user" (ngModelChange)="user = $event">
```
ngModel directive comes with property and event binding. The short form of this syntax is [(ngModel)]="user".

```html
<input type="user" name="user" [(ngModel)]="user">
```

<h2>Other types of data bindings</h2>

<h3>One-way Binding</h3>

One-way data binding in Angular (i.e. unidirectional binding) is a way to bind data from the component to the view (DOM) or vice versa - from view to the component. It is used to display information to the end-user which automatically stays synchronized with each change of the underlying data. This is similar to the one-way binding in WPF.

<h3>Two-way Binding</h3>

<img src="https://images.surferseo.art/42276c9f-580d-4b70-b137-9dcde970354f.png" alt="not found">

Two-way binding gives components in your application a way to share data. Use two-way binding to listen for events and update values simultaneously between parent and child components.

Two-way data binding gives you a way to share data between view to source and vice versa simultaneously.Two-way data binding is a combination of property binding "[]" and event binding "()" and its syntax is called banana in a box syntax [( )].

```html
<input [ngModel]="user" (ngModelChange)="user = $event">
```
ngModel directive comes with property and event binding. The short form of this syntax is [(ngModel)]="user".

```html
<input type="user" name="user" [(ngModel)]="user">
```

In this example, we have an input element with the ngModel directive bound to a variable called name. The square brackets around ngModel indicate that it's a property binding, and the parentheses indicate that it's a two-way binding. The two-way binding means that any changes made to the input element will be reflected in the name variable, and any changes made to the name variable will be reflected in the input element.


<h3>Interpolation</h3>

Data binding using double curly braces {{ }} data moves in one way from source to view.

```html
<h3>Current customer: {{ currentCustomer }}</h3>
```

<h3>Property Binding</h3>

Property binding using square brackets [] and value in one direction, from a component's property into a target element property.

```html
<button [disabled]="isDisabled">Property Binding</button>
```

<h3>Event Binding</h3>

Event binding lets you listen for and respond to user actions such as keystrokes, mouse movements, clicks, and touches.

```html
<button (click)="onSave()">Save</button>
```

<h3>Class Binding</h3>

 `[class.sale]="true/false"`,  `[class]="my-class-1 my-class-2 my-class-3"`

<h3>Style Binding</h3>

 `[style.width]="100px"`, `[style.width.px]="100"`

<h3>Attrinute Binding</h3>

`<p [attr.attribute-you-are-targeting]="expression"></p>`, `[attr.colspan]="1 + 1"`

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
