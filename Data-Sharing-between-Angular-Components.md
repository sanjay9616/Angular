<h1>Data Sharing between Angular Components</h1> - https://www.linkedin.com/pulse/different-ways-share-data-angular-mubeen-chughtai/

When building an Angular application, it's common to break it down into smaller components to keep the code manageable. However, when working with smaller components, you may need to share data between them. To do this, it's important to first define the relationship between the components. Once you have a clear understanding of the relationship, you can choose the most appropriate method to share the data.\

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

@Injectable() export class DataService {

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


<h2>3. Using View Child</h2>
<h2>4. Using State Management Libraries i.e Ngrx</h2>
<h2>5. Using @ViewChild property</h2>

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
