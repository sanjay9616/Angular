<h1>Angular Directives</h1>

How to generate directive - `ng generate directive directive-name`, or `ng g d directive-name`

**Table of Contents**

1. Introduction to Angular Directives
2. Types of directives
3. Creating Custom Directives
4. Importance of directivess

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
-  Components are directives with templates. Component directives have templates whereas Structural and Attribute directives don’t have templates. Instead, they’re tailored to DOM manipulation. The component directive comes with template or template URLs that represent something in DOM. So we can say that the component directive is a cleaner version of the Directive as it comes with a template, which is easier to use.

In component directives, you’ll find three main parameters which include:

1. **selector**: It represents the template tag which specifies the starting and end of the Component.
2. **templateUrl**: It defines which particular template is for the component.
3. **styleUrls**: It includes all the types of fashion formats for the actual component.

```ts
@Component({
    selector: 'app-pr-dashboard',
    templateUrl: './pr-dashboard.component.html',
    styleUrls: ['./pr-dashboard.component.scss']
})
export class PrDashboardComponent implements OnInit {}
```
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

<h2>Creating Custom Directives</h2>

In Angular, we can create custom directives to extend the behavior of HTML elements or components or perform a different task.

Here is a step-by-step guide to creating a custom directive in Angular:

1. First, create a new directive using the @Directive decorator, `ng generate directive directive-name`:

```ts
import { Directive } from '@angular/core';
@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective {
}
```
The selector property defines the name of the directive and specifies that it should be used as an attribute directive with the [] syntax.

2. Next, we can add behavior to the directive by using the @HostListener decorator to listen for events on the host element. In this example, we'll add a mouseenter event listener that sets the background color of the element to yellow:

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

3. Finally, we can use the directive in our component templates by adding the appHighlight attribute to an HTML element:

```html
<p appHighlight>Hover over me to highlight!</p>
```
When this component is rendered, the HighlightDirective will be applied to the <p> element, and hovering over the element will trigger the mouseenter event listener, causing the background color to change to yellow.

Overall, custom directives provide a powerful way to extend the behavior of HTML elements and components in Angular, and can be used to create reusable components, add custom attributes to elements, or modify the behavior of existing elements.

<h2>Importance of Directives</h2>

Here are some of the key benefits and importance of directives in Angular:

1. **Reusability** — Directives can be used to create reusable components that can be easily added to multiple templates. This makes it easy to create consistent UI elements across an application, and reduces the amount of duplicated code.
2. **Separation of concerns** — Directives enable developers to separate the presentation and behavior of UI elements from the underlying application logic. This makes it easier to maintain and modify the code and improves the overall structure of the application.
3. **Extensibility** — Directives can be used to extend the behavior of existing HTML elements or components, enabling developers to add new functionality without modifying the underlying code.
4. **Customization** — Directives can be used to create custom attributes that can be used to modify the behavior or appearance of HTML elements. This enables developers to create highly customizable UI components that can be easily adapted to meet the needs of different users or use cases.
5. Improved performance: Directives can be used to optimize the rendering of large or complex UI elements, enabling developers to improve the performance and responsiveness of their applications.



<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
