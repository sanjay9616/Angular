<h1>Angular Directives</h1> - https://www.linkedin.com/pulse/directives-angular-aqeel-abbas/

How to generate directive - `ng generate directive directive-name`, or `ng g d directive-name`

**Table of Contents**

1. Introduction to Angular Directives
2. Types of directives
3. Creating Custom Directives
4. Importance of directivess
5. Best practices for using directives
6. Conclusion

<h2>Introduction to Angular Directives</h2>

- Angular directives are a powerful feature of the Angular framework that allow developers to extend and modify the behavior of HTML elements.
- Directives can be used to create reusable code that can be shared across multiple components and templates, and they can also provide a way to communicate between components and the DOM.

`Angular framework that allow developers to adding new elements, removing elements, or changing the appearance of the DOM.`

<h2>Types of directives</h2>

Angular has three types of directives

1. Structural Directives
2. Attribute Directives
3. Components Directives

<h3>1. Structural directives</h3>

Structural directives are used to modify the structure of the DOM by adding, removing, or manipulating elements. Structural directives are identified by an asterisk (*) prefix before the directive name.

Some of the most commonly used structural directives in Angular are: `*ngIf, *ngFor, *ngSwitch`

1. **ngIf** directive is a structural directive in Angular that adds or removes elements from the DOM based on a given expression. If the expression evaluates to true, the element is added to the DOM; if it evaluates to false, the element is removed from the DOM.

2. **ngFor** directive is a structural directive in Angular that is used to render a list of items based on a collection in the component. The ngFor directive iterates over each product in the collection and generates a template for each product.

3. **ngSwitch** directive is a structural directive in Angular that allows us to conditionally render content based on a set of conditions.

**Examples:**

```html
<!-- ngIf Directive -->
<div *ngIf="loggedIn; else notLoggedIn">
  Welcome, {{username}}!
</div>
<ng-template #notLoggedIn>
  <div>
    Please log in to access this page.
  </div>
</ng-template>

<!-- ngFor Directive -->
<ul>
  <li *ngFor="let product of products">
    {{product}}
  </li>
</ul>

<!-- ngSwitch Directive -->
<div [ngSwitch]="color">
  <p *ngSwitchCase="'red'">The color is red.</p>
  <p *ngSwitchCase="'blue'">The color is blue.</p>
  <p *ngSwitchCase="'green'">The color is green.</p>
  <p *ngSwitchDefault>The color is unknown.</p>
</div>
```

<h3>2. Attribute Directives</h3>

Attribute Directives are used to manipulate the behavior and appearance of the DOM elements. They are used to add, remove, or modify the attributes of the HTML elements.

Some of the most commonly used Attribute Directives in Angular are:

1. **ngClass** directive in Angular is used to add or remove CSS classes dynamically based on the expressions evaluated in the template. We can use the ngClass directive to add or remove classes based on certain conditions, such as user interactions, component properties, and so on.

**Syntax**

- `[ngClass]="{'class': true}"`
- `[ngClass]="[condiion ? 'class1' : 'class2']"`
- `[ngClass]="{'class1': true, 'class2': true, 'class3': true}"`

2. **ngStyle** directive in Angular is used to add or remove styles dynamically based on the expressions evaluated in the template. We can use the ngStyle directive to add or remove styles based on certain conditions, such as user interactions, component properties, and so on.

**Syntax**

- `[ngStyle]="{'background-color':'green'}"`
- `[ngStyle]="{'background-color': condition ? 'green' : ‘red’}"`

3. **ngModel** directive is a key feature of Angular that allows two-way data binding between the model and view. It's commonly used in forms where the user input needs to be reflected in the model and vice versa.

```html
<input type="text" [(ngModel)]="name">
```

<h3>3. Component Directive</h3>

- Component directives enable developers to create reusable UI components with their own template, styles, and behavior for a consistent and modular application structure.
-  the most basic building block of angular, is a directive. It is a special kind of detective with template tag. It adds elements in the DOM as per the definition of the component.

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-component',
  template: '<h1>Welcome to My App</h1>',
})
export class HeaderComponent { }
```
```html
<app-component></app-component>
```

<h3>Creating Custom Directives</h3>

In Angular, we can create custom directives to extend the behavior of HTML elements or components or perform a different task.

Here is a step-by-step guide to creating a custom directive in Angular:

- First, create a new directive using the @Directive decorator, `ng generate directive directive-name`:

```ts
import { Directive } from '@angular/core';
@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective {
}
```
The selector property defines the name of the directive and specifies that it should be used as an attribute directive with the [] syntax.

- Next, we can add behavior to the directive by using the @HostListener decorator to listen for events on the host element. In this example, we'll add a mouseenter event listener that sets the background color of the element to yellow:

```ts
import { Directive, ElementRef, HostListener } from '@angular/core';
@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective {
  constructor(private el: ElementRef) { }
  @HostListener('mouseenter') onMouseEnter() {
    this.highlight('yellow');
  }
  private highlight(color: string) {
    this.el.nativeElement.style.backgroundColor = color;
  }
}
```

- Finally, we can use the directive in our component templates by adding the appHighlight attribute to an HTML element:

```html
<p appHighlight>Hover over me to highlight!</p>
```


<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
