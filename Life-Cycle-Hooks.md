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
  constructor(previousValue: any, currentValue: any, firstChange: boolean)
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
<h2>3. ngDoCheck()</h2>
<h2>4. ngAfterContentInit()</h2>
<h2>5. ngAfterContentInitChecked()</h2>
<h2>6. ngAfterViewInit()</h2>
<h2>7. ngAfterViewChecked()</h2>
<h2>8. ngOnDestroy()</h2>


<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
