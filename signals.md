signals:

signals are allow us to store data in state and also we can update the data in state using signals.
signals is how do we store a data into state

Types of signals:

1. Writable signal: it is a signal that can be updated and also we can read the value of this signal.
2. Readonly signal: it is a signal that can only read the value of this signal but we cannot update the value of this signal.
3. Computed signal: it is a signal that is derived from other signals. It is a signal that is computed based on other signals.

mthods of signals:
set: it is a method that is used to update the value of the signal.
updated: it is a method that is used to subscribe to the changes of the signal. It will be called whenever the value of the signal is updated.

Example of writable signal:

```typescript
import { signal } from "@angular/core";

const count = signal(0); // create a writable signal with initial value 0

console.log(count()); // read the value of the signal, output: 0
count.set(1); // update the value of the signal to 1
console.log(count()); // read the updated value of the signal, output: 1
```

Example of readonly signal:

```typescript
import { signal } from "@angular/core";
const count = signal(0); // create a writable signal with initial value 0
const readonlyCount = count.asReadonly(); // create a readonly signal from the writable signal
console.log(readonlyCount()); // read the value of the readonly signal, output: 0
readonlyCount.set(1); // this will throw an error because we cannot update a readonly signal
```

Example of computed signal:

```typescript
import { signal, computed } from "@angular/core";
const count = signal(0); // create a writable signal with initial value 0
const doubleCount = computed(() => count() * 2); // create a computed signal that
// computes the value based on the count signal
console.log(doubleCount()); // read the value of the computed signal, output: 0
count.set(1); // update the value of the count signal to 1
console.log(doubleCount()); // read the updated value of the computed signal, output: 2
```

Effects in signals:
effects are a way to run some code whenever the value of a signal changes. It is a way to react to changes in the signal. We can use effects to perform side effects such as making an API call, updating the DOM, etc.
basically hm effects ko use karte hain jab hume kisi signal ke change hone par kuch code run karna hota hai.
Example of effects in signals:

```typescript
import { signal, effect } from "@angular/core";
const count = signal(0); // create a writable signal with initial value 0
effect(() => {
  console.log(`The count is: ${count()}`); // this effect will run whenever the value of the count signal changes
});
count.set(1); // update the value of the count signal to 1, this will trigger the effect and output: The count is: 1
count.set(2); // update the value of the count signal to 2, this will
// trigger the effect and output: The count is: 2
```

linked signals:

linked signals are a way to link two signals together. It is a way to create a relationship between two signals. When the value of one signal changes, the value of the linked signal will also change.
hm linked signals ko use karte hain jab hume do signals ke beech mein relationship create karna hota hai. Jab ek signal ka value change hota hai to linked signal ka value bhi change hota hai.

Example of linked signals:

```typescript
import { signal, linkedSignal } from "@angular/core";
const count = signal(0); // create a writable signal with initial value 0
const doubleCount = linkedSignal(count, (value) => value * 2); // create a linked signal that is linked to the count signal and computes the value based on the count signal
console.log(doubleCount()); // read the value of the linked signal, output: 0
count.set(1); // update the value of the count signal to 1, this will trigger the linked signal and output: 2
count.set(2); // update the value of the count signal to 2, this will
// trigger the linked signal and output: 4
```
