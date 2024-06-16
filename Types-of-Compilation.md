<h1>Different Types of Compilation in Angular</h1>

An angular application mainly consists of HTML templates, their components which include various TypeScript files. There are some unit testing and configuration file. Whenever we run over an application, the browser cannot understand the code directly hence we have to compile our code.

Angular offers two ways to compiler your application:

- **Just-in-Time(JIT)**: which compiles your app in the browser at run time. This was the default untill Angular 8.
- **Ahead-of-Time(AOT)**: Which compiles your app and libraries at build time. this is the default since Angular 9.


<h2>AOT - Introduction</h2>

- AOT means Ahead of Time Compilation.
- All technologies Ahead of Time is a process of compiling higher-level language or intermediate language into a native machine code, which is system dependent.
- In simple words, when you serve/build your angular application, the Ahead of Time compiler converts your code during the build time before your browser downloads and runs that code. From Angular 9, by default compiling option is set to true for ahead of time compiler.

<h3>3 Phases of AOT Compilation</h3>

**1. Code Analysis:** In this phase, the typescript compiler and AOT collector creates a representation of the source. The collector doesn't attempt to interpret the metadata it collects. It represents the metadata as best it can and records errors when detects a metadata syntax violation.

    - Exression Syntaxes
    - No Arrow Functions
    - Code Folding

**2. Code Generation**: In this phase, the compiler's StaticReflector interprets the metadata collected in phase 1, performs additional validation of the metadata, and throws an error if it detects a metadata restrictios violation.

    - Generating classs
    - Functions
    - Metadata rewriting
    - Non null assertions

**3. Template Type Checking**: In ths optional phase, the Angular template compiler uses the Typescript compiler to validate the building expression in templates. You can enable this explicitly by setting the fullTemplateTypeCheck configuraion options.

<h3>Why should you use the Ahead of Time compiler</h3>

- When you are using Ahead of Time Compiler, compilation only happens once, while you build your project.
- We don’t have to ship the HTML templates and the Angular compiler whenever we enter a new component.
- It can minimize the size of your application.
- The browser does not need to compile the code in run time, it can directly render the application immediately, without waiting to compile the app first so, it provides quicker component rendering.
- The Ahead of time compiler detects template error earlier. It detects and reports template binding errors during the build steps before users can see them.
- AOT provides better security. It compiles HTML components and templates into JavaScript files long before they are served into the client display. So, there are no templates to read and no risky client-side HTML or JavaScript evaluation. This will reduce the chances of injections attacks.

<h2>AOT - Introduction</h2>

- Just in time compiler compiles each file separately and it’s mostly compiled in the browser. You don’t have to build your project again after changing your code.
- Most compiling is done on the browser side, so it will take less compiling time.
- If you have a big project or a situation where some of your components don’t come in use most of the time then you should use the Just in time compiler.
- Just in Time compiler is best when your application is in local development.

<h3>How Just in Time compiler Works?</h3>

- Initially, compiler was responsible for converting a high-level language into machine language, which would then be converted into executable code.
- Just in time compiler, compiles code at runtime which means instead of interpreting byte code at build time, it will compile byte code when that component is called.

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
