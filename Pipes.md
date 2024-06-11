<h1>Angular Pipes</h1>

- Pipes in angular is a way to transform values in an angular template.
- `Pipes are simple functions to use in expressions to accept an input value and return a transformed value.`
- There are some built in pipes. Apart from it, we can make own custom pipes also.
- Basically, pipe takes in a value or values and then returns a value. This is a good for simple transformations on data but it can be used in other unique ways.
- Pipes have multiple apis in angular which are inbuilt. However, these are two types.

<h2>1. Pure Pipes</h2>

- Pure Pipes are only called when angular detects a change in the value or parameters passed to a pipe or works only when the component is loaded. pure pipe work with only one instance of the pipe. By default a pipe is pure pipe.
- A pure pipe is a pipe that is run when a pure change is detected. A pure change is a change to a primitive JavaScript input value like strings, numbers, booleans, symbols or an object reference change.
- Pure pipes must be pure functions. Pure functions take an input and return an output. They don’t have side effects.
- Changes within objects are ignored with pure pipes. When any of these changes take place, the pipe will run and the latest change will be rendered.

<h2>2. Impure Pipes</h2>

- Impure Pipes are called for every change detection cycle no matter whether the value of parameters changes. This work with multiple instance of the pipe.
- Impure pipes are pipes that can detect changes within objects. Changes within objects include things like changing array entries or object properties.


e.g Suppose a pipe is used several times in a html code like

```html
<p> {{'Hello' | translate }}<p>
<p> {{'World' | translate }}<p>
```

**Now question in our mind how we decide that which is pure and which is impure pipe. Well this is decided by only one parameter inside pipe as below.**

```ts
@Pipe({
  name: 'sort',
  pure: false // true makes it pure and false makes it impure
})
export class myPipe implements PipeTransform {

  transform(value: any, args?: any): any {
     //your logic here and return the result
  }
}
```

<h2>3. Custom Pipes</h2>

We can make own pipes also with the help of @Pipe decorator and PipeTransform class. By overriding the transform method of this class we can make own custom pipe for custom json return type or default value , tracking changes over model , calculation over model value etc..

<a href="https://blog.bitsrc.io/mastering-custom-pipes-in-angular-31-real-world-examples-2023-c7ce8ec7faae">Mastering Custom Pipes in Angular: 31 Real-world Examples (2023)</a>

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
