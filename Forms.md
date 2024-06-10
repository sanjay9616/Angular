<h1>Angular Forms</h1> - https://medium.com/@jaydeepvpatil225/forms-in-angular-8fde7d0dcdf6

- In Angular, Forms provides a set of features that help us handle and manage user input in a structured and efficient manner.
- Forms are the main part of web applications that allow users to interact with the application and submit data to the application.

<h2>Types of Forms in Angular</h2>

Angular provides the following two types of forms:

1. Template-Driven Forms
2. Reactive Forms

<h3>1. Template-Driven Forms</h3>

- Template-driven forms are the basic forms that are suitable for the development of a limited number of fields and with simpler validation
-  In this form, each field is represented as a property in the component class.
-  You Need to import **FormsModule** from the `@angular/forms` package.

**Following are the key concepts related to validation objects, directives, and properties that we used while creating the template-driven forms in Angular.**

**ngForm Directive:** This directive represents an angular form and exposes methods and properties related to it for validation and data manipulation purposes.

**ngModel Directive:** This directive is used to achieve two-way data bindings between different form control elements.

**Validation Properties:** Angular provides different validator properties that can be applied to form controls to indicate their validation state:

1. `touched`: A boolean indicating whether the control has been touched.
2. `untouched`: The opposite of touched.
3. `valid`: A boolean indicating whether the control’s value is valid.
4. `invalid`: The opposite of valid

**Validation Directives:** Angular provides several built-in validation directives that can be used with ngModel to perform validation. Some common ones include:

1. `required`: Ensures the control has a non-empty value.
2. `min length and max length`: Specifies the minimum and maximum length for the value.
3. `pattern`: Validates the value against a regular expression.
4. `email`: Validates that the value is a valid email address.

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
