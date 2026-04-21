standAlone Component

standAlone Component aik a Angular Component hota hai jo apne aap me complete hota hai aur kisi module ke andar nahi hota. Iska use tab kiya jata hai jab hume ek chhota aur reusable component banana hota hai jo kisi specific functionality ko handle karta hai.

StandAlone Component banane ke liye, hum @Component decorator ka use karte hain aur usme standalone: true property set karte hain. Isse Angular ko pata chal jata hai ki ye component standalone hai aur kisi module ke andar nahi hai.

Example:

```typescript
import { Component } from "@angular/core";
@Component({
  selector: "app-standalone",
  template: `<h1>This is a StandAlone Component</h1>`,
  standalone: true,
})
export class StandAloneComponent {
  // Component logic goes here
}
```

Is example me, StandAloneComponent ek standalone component hai jo apne aap me complete hai. Iska selector 'app-standalone' hai aur iska template ek simple heading display karta hai.
StandAlone Component ka use karne ke liye, hume is component ko kisi module me import karne ki zarurat nahi hoti. Hum ise directly apne application me use kar sakte hain.
Example of using StandAlone Component:

```html
<app-standalone></app-standalone>
```

Is example me, humne StandAloneComponent ko directly apne template me use kiya hai. Jab hum is component ko render karenge, to hume "This is a StandAlone Component" heading dikhai degi.
StandAlone Component ka use karne ke fayde:

1. Reusability: StandAlone Component ko hum apne application ke kisi bhi part me reuse kar sakte hain bina kisi module ke andar import kiye.
2. Simplicity: StandAlone Component chhota aur simple hota hai, jise banana aur maintain karna asaan hota hai.
3. Encapsulation: StandAlone Component apne aap me complete hota hai, isliye uski functionality aur styling dusre components se alag hoti hai, jisse encapsulation achieve hota hai.
4. Performance: StandAlone Component ko directly use karne se, Angular ko us component
   ko load karne ke liye kisi module ke andar import karne ki zarurat nahi hoti, jisse application ki performance improve hoti hai.
   Overall, StandAlone Component Angular me ek powerful feature hai jo hume chhote aur

AppComponent is by default a StandAlone Component in Angular. Jab hum Angular application create karte hain, to AppComponent automatically standalone hota hai. Iska matlab hai ki AppComponent apne aap me complete hota hai aur kisi module ke andar nahi hota.
