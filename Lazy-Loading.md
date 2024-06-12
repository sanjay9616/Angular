<h1>Lazy Loading in Angular</h1>

- Lazy Loading is a technique in Angular that allows you to load certain parts of your application only when they are needed, rather than loading the entire application upfront. This can significantly improve the performance of your application, especially for larger applications that have a lot of modules.
- With Lazy Loading, you can split your application into separate modules, each containing a different set of features or functionality. Then, you can configure Angular to load each module on-demand, as the user navigates to different parts of the application.
- To implement Lazy Loading in Angular, you need to use the loadChildren property in your routing configuration. This property takes a string that represents the path to the module that should be loaded lazily. For example:

```ts
const routes: Routes = [
 { path: '', component: HomeComponent },
 { path: 'lazy', loadChildren: () => import('./lazy/lazy.module').then(m => m.LazyModule) }
];
```

- In this example, the loadChildren property is used to load the LazyModule module lazily when the user navigates to the /lazy path. The import() function is used to dynamically load the module, and the then() function is used to retrieve the LazyModule from the loaded module.
- Lazy Loading can be a powerful tool for improving the performance of your Angular application, especially for larger applications that have a lot of modules. By loading only the parts of the application that are needed, you can reduce the initial load time and improve the user experience.

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
