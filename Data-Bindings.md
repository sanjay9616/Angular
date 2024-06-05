<h1>Data Bindings in Angular</h1>

Angular provides three categories of data binding according to the direction of data flow:

<h2>1. From source to view</h2>

```ts
// SOURCE
value: string = 'From source to view data binding';
```
```html
<!-- VIEW -->
<h1>{{value}}</h1>
```

<h2>2. From view to source</h2>

```html
<!-- VIEW -->
<input type="text" (input)="onInputChange($event)">
```
```ts
// SOURCE
value: string = ''
onInputChange(value: string) {
    this.value = value
}
```

<h2>3. In a two-way sequence of view to source to view</h2>

```html
<!-- VIEW -->
<input type="text" (input)="onInputChange($event)">
<h1>{{value}}</h1>
```
```ts
// SOURCE
value: string = ''
onInputChange(value: string) {
    this.value = value
}
```

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

<h3>Class Binding</h3>

<h3>Style Binding</h3>

<h3>Attrinute Binding</h3>

<h3>Event Binding</h3>

<h3>One-way Binding</h3>

<h3>Two-way Binding</h3>

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
