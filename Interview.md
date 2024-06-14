<h1>Angular Interview Questions and Answers</h1>

### Table of Contents

| No. | Questions                                                                                                                             |
| --- | ------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is a data binding](#What-is-a-data-binding)                                                                                     |
| 1   | [What is interpolation](#What-is-interpolation)                                                                                       |
| 1   | [How do you categorize data binding types](#How-do-you-categorize-data-binding-types)                                                 |
| 1   | [What is the difference between interpolated content and innerHTM](#What-is-the-difference-between-interpolated-content-and-innerHTM) |

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




<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
