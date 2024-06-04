<h1>Different Types of Angular CLI Commands</h1>

There are three types of Angular CLI commands

<h2>1. Schematics Commands</h2>

Schematics commands are based on a tool called Schematics that comes from the `@angular-devkit/schematics package`. Schematics is the underlying tool the Angular CLI uses to scaffold a new Angular workspace (ng new), generate blueprints (ng generate), update/migrate existing code (ng update), and add some frameworks support to an Angular application (ng add). It's all about code generation.

**examples** - `ng new, ng add, ng generate, ng update` etc

<h3>ng generate <schematic>:</h3>

Generates and/or modifies files based on a schematic, This command has the following sub-commands.

`ng generate component [name]` or `ng generate c [name]`: Creates a new, generic component definition in the given project.

`ng generate class [name]` or `ng generate cl [name]`: Creates a new, generic class definition in the given project.

`ng generate application [name]` or `ng generate app [name]`: Generates a new basic application definition in the "projects" subfolder of the workspace.

**and other sub-commands mentioned below:**

`ng generate directive [name] / ng generate d [name]`,`ng generate guard [name] / ng generate g [name]`,`ng generate interceptor [name]`, `ng generate module [name] / ng generate m [name]`, `ng generate pipe [name] / ng generate p [name]`, `ng generate service [name] / ng generate s [name]`, `ng generate app-shell`, `ng generate config [type]`, `ng generate enum [name] / ng generate e [name]`, `ng generate environments`, `ng generate interface [name] [type] / ng generate i [name] [type]`, `ng generate library [name] / ng generate lib [name]`, `ng generate resolver [name] / ng generate r [name]`, `ng generate service-worker`, `ng generate web-worker [name]`

</h2>2. Architect Commands:</h2>

Architect commands are based on a tool called Architect that is published under the `@angular-devkit/architect` package name. Architect helps the Angular CLI lint (ng lint), test (ng test, ng e2e), serve (ng serve), build (ng build), and deploy (ng deploy) our Angular applications. It's all about running complex tasks.

**examples** - `ng build, ng deploy, ng e2e,ng lint,ng run,ng serve,ng test,ng xi18n` etc


<h2>3. Native Commands:</h2>

Native commands are general Angular CLI commands. They are native to the Angular CLI in the sense that they don't rely on other tools/packages to be executed. Displaying our packages' versions (ng version), opening the official documentation (ng doc), reading and setting some values in the angular.json file (ng config), or displaying the list of available commands and their description (ng help) do not require the use of any specific tool.

**examples** - `ng config,ng doc,ng version, ng analytics, ng help` etc


<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
