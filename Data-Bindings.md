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

<h2>Interpolation</h2>
<h2>Property Binding</h2>
<h2>Class Binding</h2>
<h2>Style Binding</h2>
<h2>Attrinute Binding</h2>
<h2>Event Binding</h2>
<h2>One-way Binding</h2>
<h2>Two-way Binding</h2>

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
