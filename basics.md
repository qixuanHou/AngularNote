* <a href="#howload">How Angular Loads</a>
* <a href="#component">Component</a>


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

### Module 
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

