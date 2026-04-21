Routing in angular is a powerful feature that allows you to navigate between different views or components in your application. It enables you to create a single-page application (SPA) where the content can change dynamically without requiring a full page reload.

hme routing ko use karne ke liye, aapko Angular Router module ko import karna hoga. Iske baad, aap apne application ke routes ko define kar sakte hain. Routes ek array hota hai jisme aap har route ke path aur usse associated component ko specify karte hain.

path: ye route ka URL path hota hai, jise user browser me type karega ya jise aap programmatically navigate karenge.
component: ye us component ko specify karta hai jo is route ke liye render hoga.
Example:

```typescript
import { NgModule } from "@angular/core";
import { RouterModule, Routes } from "@angular/router";
import { HomeComponent } from "./home/home.component";

const routes: Routes = [{ path: "home", component: HomeComponent }];
```

Is example me, humne ek route define kiya hai jiska path "home" hai aur usse associated component HomeComponent hai. Jab user "/home" URL par navigate karega, to HomeComponent render hoga.

Aap multiple routes bhi define kar sakte hain, aur unhe ek array me rakh sakte hain.

routerLink: Angular me, aap routerLink directive ka use karke navigation links create kar sakte hain. Ye directive aapko HTML templates me links banane ka tariqa deta hai jo Angular Router ke through navigate karte hain.

Example:

```html
<a routerLink="/home">Go to Home</a>
```

Is example me, humne ek anchor tag banaya hai jisme routerLink directive ka use kiya gaya hai. Jab user is link par click karega, to Angular Router "/home" path par navigate karega aur HomeComponent render hoga.

Router-outlet: Angular me, router-outlet directive ka use karke aap apne application ke layout me ek placeholder create kar sakte hain jahan par routed components render honge. Ye directive aapko dynamic content display karne ka tariqa deta hai jab user different routes par navigate karta hai.
Example:

```html
<router-outlet></router-outlet>
```

Is example me, humne router-outlet directive ka use kiya hai. Jab user kisi route par navigate karega, to us route se associated component is router-outlet ke andar render hoga. Aap apne application ke layout me multiple router-outlet bhi use kar sakte hain agar aapko nested routing ki zarurat hai.
In summary, Angular routing allows you to create a seamless navigation experience in your application by defining routes, using routerLink for navigation, and utilizing router-outlet to display the appropriate components based on the current route.

routerlinkActive: Angular me, routerLinkActive directive ka use karke aap apne navigation links ko active state me style kar sakte hain jab user us route par hota hai. Ye directive aapko CSS classes apply karne ka tariqa deta hai jab user kisi specific route par navigate karta hai.
Example:

```html
<a routerLink="/home" routerLinkActive="active">Go to Home</a>
```

Is example me, humne routerLinkActive directive ka use kiya hai. Jab user "/home" route par navigate karega, to "active" CSS class is anchor tag par apply ho jayegi. Aap apne CSS me "active" class ko style kar sakte hain taaki active links visually distinguishable ho sakein. Aap multiple classes bhi specify kar sakte hain routerLinkActive directive me, jaise ki "routerLinkActive="active highlight"".

navigate method: Angular Router me, aap navigate method ka use karke programmatically navigation kar sakte hain. Ye method aapko code ke through routes par navigate karne ka tariqa deta hai, jaise ki button click events ya kisi specific logic ke basis par.
Example:

```typescript
import { Component } from "@angular/core";
import { Router } from "@angular/router";
@Component({
  selector: "app-example",
  template: `<button (click)="goToHome()">Go to Home</button>`,
})
export class ExampleComponent {
  constructor(private router: Router) {}
  goToHome() {
    this.router.navigate(["/home"]);
  }
}
```

Is example me, humne ek button banaya hai jisme click event par goToHome method call hoti hai. goToHome method me, hum Angular Router ke navigate method ka use karke "/home" route par navigate kar rahe hain. Jab user button par click karega, to HomeComponent render hoga. Aap navigate method me additional options bhi specify kar sakte hain, jaise ki query parameters ya route parameters, taaki aap apne navigation ko aur bhi dynamic bana sakein.
