* <a href="#howload">How Angular Loads</a>
* <a href="#component">Component</a>
* <a href="#databinding">Databinding</a>
* <a href="#directives">Directives</a>


### How Angular loads?<a name="howload"></a>
* Angular is a JavaScript Framework which allows you to create reactive Single-Page-Applications. Only have one html file to avoid long loading time, javascript changes DOM dynamically 
* main.ts -> app.module.ts (contains all the components) -> app.component.html/ app.component.ts/

### Component<a name="component"></a>
* create a folder for a new component, which contains .ts .html .css
* inside .ts file
``` typescript
import { Component } from '@angular/core';
@Component({
  selector: 'app-server',
  templateUrl: './server.component.html',
})
export class ServerComponent {

}
```
* ng generate component servers (servers is component name)

#### Module 
* sample app.module.ts
``` typescript
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent } from './app/.component';
import { ServerComponent } from './server/server.component';
@NgModule({
  declarations: [
    AppComponent,
    ServerComponent,
  ],
  imports: [BrowserModule],
  providers: [].
  bootstrap: [AppComponent]
})
export class AppModule { }
```
* add server component to the parent component - app.component.html
``` html
<app-server/><app-server>
```
#### Component Selector
```Typescript
@Component({
    selector: "inventory-table-new",
    templateUrl: "./inventory-table.component.html",
})
```
```html
<inventory-table-new>
```
```Typescript
@Component({
    selector: "[inventory-table-new]",
    templateUrl: "./inventory-table.component.html",
})
```
```html
<div class="inventory-table-new">
```

### Databinding<a name="databinding"></a>
TypeScript -> HTML 
* string interpolation {{ data }}
* property binding [property] = "data"
HTML -> TypeScript
* event building (event) = "expression"
Two-way bindings 
* [(ngModel)] = "data"
```HTML
<input
  type="text"
  (input) = "onUpdateServerName($event)">
<button
  [disabled] = "!allowNewServer"
  [click] = "onCreateServer()">Add Server</button>
```
two way binding
```HTML
<input
  type="text"
  [(ngModel)] = "serverName">
```

### Directives<a name="directives"></a>
Directives are Instructions in the DOM
a sample structure
```HTML
<p appTurnGreen>Receives a green backgrounds</p>
```
```HTML
@Directives({
  selector: '[appTurnGreen]'
})
export class TurnGreenDirective {
  ...
}
```
existing directives demonstration
```HTML
<p *ngIf="displayOrNot">Server </p>
```
```HTML
<p *ngIf="displayOrNot; else noServer">Server </p>
<ng-template #noServer>
  <p>...</p>
</ng-template>
```
```HTML
<p 
   [ngStyle]="{backgroundColor: getColor()}"
   [ngClass]="{online: serverStatus}"
   ></p>
```
