<h1>Component Life Cycle Hooks</h1>

Angular has 8 lifecycle hooks that help us in every situation where we would like to write some code on a specific event.

- Each interface has a single hook method whose name is the interface name plus prefixed with ng. So, before using the interface method, we must have to implement the respective interface.
- For example, the OnChange interface has a hook method named ngOnChange() that Angular calls shortly after creating the component. Evermore, it’s required to import SimpleChanges for the OnChange method only.

<img src="https://media.licdn.com/dms/image/C5612AQHH-keKNUYirw/article-inline_image-shrink_1500_2232/0/1648102509784?e=1723075200&v=beta&t=PwfmG35SAngielKeuHWn641XwJOFkx7aGzZTwNiwT30" alt="not found">

<h2>1. ngOnChanges()</h2> - https://www.stackchief.com/blog/ngOnChanges%20Example%20%7C%20Angular

- ngOnChanges called before `ngOnInit()` and whenever one/more data-bound input properties change.
- It means, whenever any `@input` decorator changed `from the parent component than` the code under this function will be triggered.
- Whenever any `@output` decorator changed from the child component than the code under this `function will not be triggered`.
- This means if you don't have any `@Input` properties on a child, ngOnChanges will never get called.
- It’s required to import SimpleChanges for the OnChange method only.


<h2>2. ngOnInit()</h2>
<h2>3. ngDoCheck()</h2>
<h2>4. ngAfterContentInit()</h2>
<h2>5. ngAfterContentInitChecked()</h2>
<h2>6. ngAfterViewInit()</h2>
<h2>7. ngAfterViewChecked()</h2>
<h2>8. ngOnDestroy()</h2>


<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
