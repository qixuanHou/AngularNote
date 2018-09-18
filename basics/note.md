* <a href="#whatisangular">What is Angular</a>
* <a href="#projectsetup">Project Setup</a>
* <a href="#typescript">Typescript</a>


### What is Angular?<a name="whatisangular"></a>
* Angular is a JavaScript Framework which allows you to create reactive Single-Page-Applications. Only have one html file to avoid long loading time, javascript changes DOM dynamically 
* Angular Versions – Angular 1 -> Angular 2 (entirely rewrite), other versions have more functions 
### Project Setup<a name="projectsetup"></a>
* Start Angular project
``` 
npm install -g @angular/cli
ng new my-first-app test
cd my-first-app
ng serve
```
* <app-root> which will be replaced by dynamic script
### Typescript<a name="typescript"></a>
* typescript will be eventually converted into JavaScript during compiling time 
* type
``` typescript
let aString: string;
aString = “asdfasd”;
let aString = “asdfasd”;
```
* class
``` typescript
class Car {
          engineName: string;
	gears: number;
	private speed: number;

	constructor (speed: number) {
		this.speed = speed || 0;
          }

	accelerate (): void {
	          this.speed++;
          }

          Static numberOfWheels (): number {
	          Return 4;
          }
}
```
``` typescript
let car = new Car(5);
console.log(Car.numberOfWheels());
```
* interface – contract defines what variables and functions are required 
``` typescript
Interface User {
	username: string;
	password: string;
	passwordConfirmed?: string; //optional
}
let user:User;
user = {username: “max”, password: “aasasd”};
```
``` typescript
Interface CanDrive {
	accelerate(speed: number): void;
}
let car:CanDrive = {
	accelerate: function (speed: number) {
          	…
          }
}
```
* generics – be flexible regarding  
``` typescript
let numberArray: Array<number>;
numberArray = [1,2,3];
```
* modules – splitting the code into several files and then link them back together 
``` typescript
Export class ExportedClass {
	// This class will be exported
}
```
