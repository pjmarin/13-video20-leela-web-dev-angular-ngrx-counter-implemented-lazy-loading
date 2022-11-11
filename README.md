SOURCE: https://www.youtube.com/watch?v=sfrLeTfa7fI&list=PL_euSNU_eLbdg0gKbR8zmVJb4xLgHR7BX&index=7

En este video hemos implementado lazy loading.

Para ello hemos eliminado en app.module.ts los imports de los componentes de counter y posts, y tambien los hemos eliminado del array "declarations".
Los hemos movido a las carpetas /counter y /posts, dentro de las cuales hemos creado un archivo counter.module.ts y posts.module.ts respectivamente.

Tambien, en el archivo app-routing-module.ts, dejamos por una parte, en las rutas, la propiedad "path" con el valor "counter" y "post", pero quitamos el componente en el caso de counter, y el componente y los children en el caso de post, y los movemos tambien a counter.module.ts y posts.module.ts, donde definiremos la variable routes que es un array de objetos, en cada uno de los cuales, la propiedad "path" no ira ahora con el valor counter o posts, sino que ira con el valor vacio "" (es decir, a partir de la ruta "counter" por ejemplo, definida en app-routing-module.ts, la ruta vacio coincide con el componente counter implementado en el counter.module.ts.
Importaremos en el modulo counter los componentes: 
- CounterComponent
- CounterOutputComponent
- CounterButtonsComponent
- CustomCounterInputComponent

ademas de los modulos CommonModule, FormsModule, y por supuesto RouterModule, el cual implementaremos a traves de RouterModule.forChild(routes).

Importaremos en el modulo posts los componentes: 
- PostsListComponent
- AddPostComponent
- EditPostComponent

ademas de los modulos CommonModule, ReactiveFormsModule (porque lo utilizamos para el formulario para agregar o editar un post), y tambien por supuesto RouterModule, el cual implementaremos a traves de RouterModule.forChild(routes).

Agregaremos tambien los children en este modulo de posts

# LeelaWebDevNgrx

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 14.2.8.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
