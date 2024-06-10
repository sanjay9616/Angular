<h1>Angular Directives</h1>

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

<h3>Structural directives</h3>

Structural directives are used to modify the structure of the DOM by adding, removing, or manipulating elements. Structural directives are identified by an asterisk (*) prefix before the directive name.

Some of the most commonly used structural directives in Angular are: `*ngIf, *ngFor, *ngSwitch`

**ngIf** directive is a structural directive in Angular that adds or removes elements from the DOM based on a given expression. If the expression evaluates to true, the element is added to the DOM; if it evaluates to false, the element is removed from the DOM.

**ngFor** directive is a structural directive in Angular that is used to render a list of items based on a collection in the component. The ngFor directive iterates over each product in the collection and generates a template for each product.

**ngSwitch** directive is a structural directive in Angular that allows us to conditionally render content based on a set of conditions.

**Examples:**

```html
<!-- ngIf -->
<div *ngIf="loggedIn; else notLoggedIn">
  Welcome, {{username}}!
</div>
<ng-template #notLoggedIn>
  <div>
    Please log in to access this page.
  </div>
</ng-template>

<!-- ngFor -->
<ul>
  <li *ngFor="let product of products">
    {{product}}
  </li>
</ul>

<!-- ngSwitch -->
<div [ngSwitch]="color">
  <p *ngSwitchCase="'red'">The color is red.</p>
  <p *ngSwitchCase="'blue'">The color is blue.</p>
  <p *ngSwitchCase="'green'">The color is green.</p>
  <p *ngSwitchDefault>The color is unknown.</p>
</div>
```

<h3>Attribute Directives</h3>



<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
