<h1>Component Life Cycle Hooks</h1>

Angular has 8 lifecycle hooks that help us in every situation where we would like to write some code on a specific event.

- Each interface has a single hook method whose name is the interface name plus prefixed with ng. So, before using the interface method, we must have to implement the respective interface.
- For example, the OnChange interface has a hook method named ngOnChange() that Angular calls shortly after creating the component. Evermore, it’s required to import SimpleChanges for the OnChange method only.

<img src="https://media.licdn.com/dms/image/C5612AQHH-keKNUYirw/article-inline_image-shrink_1500_2232/0/1648102509784?e=1723075200&v=beta&t=PwfmG35SAngielKeuHWn641XwJOFkx7aGzZTwNiwT30" alt="not found">

<h2>1. ngOnChanges()</h2>

- ngOnChanges called before `ngOnInit()` and whenever one/more data-bound input properties change.
- It means, whenever any `@input` decorator changed `from the parent component` tha` the code under this function will be triggered.
- Whenever any `@output` decorator changed from the child component than the code under this `function will not be triggered`.
- This means if you don't have any `@Input` properties on a child, ngOnChanges will never get called.
- It’s required to import SimpleChanges for the OnChange method only.

```ts
// parent.component.ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-parent',
  templateUrl: './parent.component.html',
  styleUrls: ['./parent.component.scss']
})
export class ParentComponent {

  data: number = 0;

  changeFromParent() {
    this.data += 1;
  }
}
```
```html
<!-- parent.component.html -->
<div>
    <button type="button" (click)="changeFromParent()">Change from parent</button>
    <app-child [parentData]=data></app-child>
</div>
```
```ts
// child.component.ts
import { Component, Input, SimpleChanges } from '@angular/core';

@Component({
  selector: 'app-child',
  templateUrl: './child.component.html',
  styleUrls: ['./child.component.scss']
})
export class ChildComponent {

  @Input() parentData!: number;

  changeFromChild() {
    this.parentData -= 1;
  }

  ngOnChanges(changes: SimpleChanges) {
    console.log('ngOnChanges', changes);
  }
}
```
```html
<!-- child.componen.html -->
<button type="button" (click)="changeFromChild()">Change from child</button>
<div>parentData - {{parentData}}</div>
```
The SimpleChanges instance looks like this...

```ts
class SimpleChange {
  constructor(previousValue: any, currentValue: any, firstChange: boolean) {}
  previousValue: any
  currentValue: any
  firstChange: boolean
  isFirstChange(): boolean
}
```
Every time ngOnChanges() is called, the SimpleChanges instance captures the parentData's:

`{ "previousValue": 0, "currentValue": 1, "firstChange": false }`

- **previousValue**
- **currentValue**
- **firstChange** (true the first time ngOnChanges is called)

**What about multiple inputs?**

Each bound variable is returned with its corresponding SimpleChanges instance in a single object.

```ts
//SimpleChanges object with multiple inputs
{
  parentData: { currentValue: 1, firstChange: false, previousValue: 0 },
  firstName: { currentValue: "Sam", firstChange: false, previousValue: "Eric" },
  age: { currentValue: 25, firstChange: false, previousValue: 20 }
}
```

**When should you use ngOnChanges?**

- Use ngOnChanges whenever you want to detect changes from a variable decorated by @Input. Remember that only changes from the parent component will trigger this function.
- Also remember that changes from the parent still update the child value even without implementing ngOnChanges. ngOnChanges simply adds the benefit of tracking those changes with previous and current value.


<h2>2. ngOnInit()</h2>

- ngOnInit is there to give us a signal that Angular has finished initializing the component and now we can perform our needed operations.
- Therefore, I consider it as one of the important hooks from a list of Angular lifecycle hooks and very useful, as well.
- This hook initializes data for a component.
- After setting the input values, this hook gets its call.
- This hook is added by default by Angular CLI to all the components.
- It is called only for once.
- As it is already said, this hook gets initialization after ngOnChanges that means all the properties ngOnInit can use all its properties. Any of the child directive properties cannot be used before this hack gets triggered.

```ts
ngOnInit(): void {
  console.log(“ngOnInit running”);
}
```

<h2>3. ngDoCheck()</h2>

- Used to detect changes that angular will not detect on its own. It is called immediately after ngOnChanges as well as the first ngOnInIt.
- Since it is called multiple times it is an expensive lifecycle method. It is advisable not to use ngDoCheck with ngOnChanges since it may be very expensive.
- ngDoCheck can get changes even when a property or array changes to data that is bound to a component or a directive.

```ts
import { Component, Input, SimpleChanges } from '@angular/core';

@Component({
  selector: 'app-child',
  templateUrl: './child.component.html',
  styleUrls: ['./child.component.scss']
})
export class ChildComponent {

  @Input() parentData!: number;

  constructor() {
    console.log('constructor')
  }

  ngOnChanges(changes: SimpleChanges) {
    console.log('ngOnChanges', changes);
  }

  ngOnInit() {
    console.log('ngOnInit');
  }

  ngDoCheck() {
    console.log('ngDoCheck')
  }

  changeFromChild() {
    this.parentData -= 1;
  }
}
```
**Output**
```
constructor
ngOnChanges
ngOnInit
ngDoCheck
// when parentData updated from parent component
ngOnChanges
ngDoCheck
ngOnChanges
ngDoCheck
// when parentData updated from child component
ngDoCheck
ngDoCheck
```

<h2>4. ngAfterContentInit()</h2>

- ngAfterContentInit, as the name suggested, responds when the angular app projects content into the component’s view and the view is ready.
- It is called once after the first ngDoCheck().
- It is also known as a component-only hook.

```ts
ngAfterContentInit() {
  console.log("ngAfterContentInit");
}
```

<h2>5. ngAfterContentInitChecked()</h2>

- ngAfterContentChecked, as its name suggested respond after the app checks the content actually projected into the component.
- It called after ngAfterContentInit and every subsequent check.

```ts
ngAfterContentInitChecked() {
  console.log("ngAfterContentInitChecked");
}
```

<h2>6. ngAfterViewInit()</h2>

- ngAfterViewInit, responds after app initialized and all the views of component has been ready.
- It called once after the first ngAfterContentChecked.

```ts
ngAfterViewInit() {
  console.log("ngAfterViewInit");
}
```

<h2>7. ngAfterViewChecked()</h2>

- ngAfterViewChecked, responds after app checks all the parent and child views of components.
- It called after the ngAfterViewInit and every subsequent call of ngAfterContentChecked

```ts
ngAfterViewChecked() {
  console.log("ngAfterViewChecked");
}
```

<h2>8. ngOnDestroy()</h2>

- The ngDestory, as its name suggested, will use to do clean-up just before the angular app destroys everything.
- Furthermore, it will detach the events, unsubscribe the Observables, etc to avoid any memory leaks.
- It is called just before the angular app destroys everything like the directive and components.

```ts
ngOnDestroy() {
  console.log("ngOnDestroy");
}
```

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
