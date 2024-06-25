<h1>Data Sharing between Angular Components</h1>

When building an Angular application, it's common to break it down into smaller components to keep the code manageable. However, when working with smaller components, you may need to share data between them. To do this, it's important to first define the relationship between the components. Once you have a clear understanding of the relationship, you can choose the most appropriate method to share the data.

1. Using @Input @Output decorator for Parent Child Components.
2. Using a Shared Service.
3. Using State Management Libraries i.e Ngrx.
4. Using Local Storage or Session Storage.
5. Using @ViewChild property.
6. 9 ways to pass data through Angular RouterState.

<h2>1. Using @Input @Output decorator for Parent Child Components</h2>

The @Input and @Output decorators are used to pass data between components that have a parent-child relationship. @Input allows a parent component to pass data down to a child component, while @Output allows a child component to emit an event to the parent component.

- Use `@Input` when you need to pass data down from a parent component to a child component. This approach is useful when you want to reuse a child component in different parts of your application.

- Use `@Output` when you need to emit an event from a child component to a parent component. This approach is useful when you want to notify the parent component of a change that occurred in the child component.

**Parent component HTML:**
```html
<app-child
    [data]="parentData"
    (event)="parentMethod($event)">
</app-child>
```
**Parent component TS:**
```ts
parentData: any = { name: 'John', age: 30 };

public parentMethod(event: any): void {
    console.log('Event received from child:', event);
}
```
**Child component TS:**
```ts
@Input() data: any;
@Output() event: EventEmitter<any> = new EventEmitter<any>();

public childMethod(): void {
    this.event.emit('Event data from child');
}
```

<h2>2. Using a Shared Service</h2>

- Services are used to share data between components that do not have a parent-child relationship. By creating a shared service, you can keep your data centralized and easily accessible by any component that needs it.

- Use services when you need to share data between components that are not directly related, or when you want to avoid passing data through several layers of components.

```ts
import { Injectable } from '@angular/core';
import { BehaviorSubject, Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class DataService {

  private data$: BehaviorSubject<any> = new BehaviorSubject<any>({});

  public getData(): Observable<any> {
    return this.data$.asObservable();
  }

  public setData(data: any): void {
    this.data$.next(data);
  }
}
```
**Component TS**
```ts
import { Component, OnInit } from '@angular/core';
import { DataService } from '../data.service';

@Component({
  selector: 'app-my-component',
  templateUrl: './app-my-component',
  styleUrls: ['./app-my-component']
})

export class MyComponent implements OnInit {

  public data: any = {};

  constructor(private dataService: DataService) { }

  ngOnInit(): void {
    this.dataService.getData().subscribe((data) => {
      this.data = data;
    });
  }

  public updateData(): void {
    this.dataService.setData({ name: 'John', age: 30 });
  }
}
```


<h2>3. Using State Management Libraries i.e Ngrx</h2>

- NgRx is a state management library for Angular applications. It provides a way to manage application state in a centralized location and allows for easy data sharing between components.
- Use NgRx when you need to manage complex application state or when you want to keep your data and business logic separate from your components.

```ts
// app.module.ts
import { counterReducer } from './shared/store/counter.reducer';
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { StoreModule } from '@ngrx/store';

@NgModule({
  declarations: [],
  imports: [
    BrowserModule,
    StoreModule.forRoot({ counter: counterReducer })
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```
```ts
// counter.store.ts
export const initialState = {
    counter: 0
}
```
```ts
// counter.reducer.ts
import { createReducer, on } from "@ngrx/store";
import { decrement, increment } from "./counter.actions";
import { initialState } from "./counter.store";


const _counterReducer = createReducer(initialState,
    on(increment, (state) => {
        return {
            ...state,
            counter: state.counter + 1
        }
    }),
    on(decrement, (state) => {
        return {
            ...state,
            counter: state.counter - 1
        }
    }),
)

export function counterReducer(state: any, action: any) {
    return _counterReducer(state, action);
}
```
```ts
// counter.actions.ts
import { createAction, props } from "@ngrx/store";
export const increment = createAction("increment");
export const decrement = createAction("decrement");
```
```ts
// Component TS:
import { Component } from '@angular/core';
import { Store } from '@ngrx/store';
import { decrement, increment } from 'src/app/shared/store/counter.actions';

@Component({
  selector: 'app-counterbutton',
  templateUrl: './counterbutton.component.html',
  styleUrls: ['./counterbutton.component.scss']
})
export class CounterbuttonComponent {

    public counter$ = this.store.select('counter');

  constructor(private store: Store<{ counter: { counter: number } }>) { }

  ngOnInit() { }

  onIncrement() {
    this.store.dispatch(increment());
  }

  onDecrement() {
    this.store.dispatch(decrement());
  }
}
```
```html
<!-- Component HTML: -->
<h1>Counter Application</h1>
<button type="button" (click)="onIncrement()">Increment (+)</button>
<button type="button" (click)="onDecrement()">Decrement (-)</button>
```

<h2>4. Using Local Storage or Session Storage</h2>

- Local storage is a browser API that allows you to store key-value pairs in the user's browser. It can be used to store small amounts of data that need to persist between page reloads.
- Use local storage when you need to store small amounts of data that need to persist between page reloads, such as user preferences or login information.

```html
<!-- component HTMl -->
<div>{{ data.name }} is {{ data.age }} years old.</div>
<button (click)="updateData()">Update Data</button> `
```
```ts
// component TS
export class MyComponent implements OnInit {

  data: any = {};

  ngOnInit(): void {
    const data = JSON.parse(localStorage.getItem('data') || '{}');
    this.data = data;
  }

  updateData(): void {
    const newData = {
      name: 'John',
      age: 30
    };
    this.data = newData;
    localStorage.setItem('data', JSON.stringify(newData));
  }
}
```

<h2>5. Using @ViewChild property</h2>

- `@ViewChild` is used to access the properties and methods of a child component from the parent component. This approach is useful when you need to get data from a child component that is several levels deep in the component hierarchy.
- Use `@ViewChild` when you need to access the properties and methods of a child component from the parent component. This approach is useful when you need to get data from a child component that is several levels deep in the component hierarchy.

```html
<!-- Child HTML -->
<h2>{{ title }}</h2>
```
```ts
// Child TS
import { Component, Input } from '@angular/core';
@Component({
  selector: 'app-child',
  templateUrl: './child.component.html',
  styleUrls: ['./child.component.scss']
})

export class ChildComponent {

  @Input() title!: string;

  public childMethod() {
    console.log('Child method called');
  }
}
```
```html
<!-- Parent HTML -->
<div>
    <button (click)="parentMethod()">Parent Method</button>
    <app-child #childComponent [title]="title"></app-child>
</div>
```
```ts
// Parent TS
import { Component, ViewChild } from '@angular/core';
import { ChildComponent } from './child.component';
@Component({
  selector: 'app-parent',
  templateUrl: './parent.component.html',
  styleUrls: ['./parent.component.scss']
})

export class ParentComponent {

  @ViewChild('childComponent') child: ChildComponent;
  public title = 'Child Component Title';

  parentMethod() {
    console.log('Parent method called');
    this.child.childMethod();
  }
}
```

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/Router.md">6. 9 ways to pass data through Angular RouterState</a></h2>

**Summary:**

These are just a few examples of how you can share data between components in Angular. Depending on your use case, some approaches may be more appropriate than others. The Input and Output decorators are the simplest way to share data between parent and child components, while using a shared service provides more flexibility and allows you to share data between any components in your application. State management libraries like NgRx provide even more powerful tools for managing and sharing application data, but may come with a steeper learning curve. Finally, using local storage or session storage can be a good option for sharing small amounts of data between components, but may not be suitable for larger amounts of data or more complex use cases.


<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
