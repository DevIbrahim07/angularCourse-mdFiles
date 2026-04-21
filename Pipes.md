Pipes in Angular:
Pipes are a powerful feature in Angular that allow you to transform data in your templates. They are used to format data before displaying it to the user. Angular provides several built-in pipes, and you can also create your own custom pipes.

Built-in Pipes:

1. DatePipe: Formats a date value according to locale rules.
2. UpperCasePipe: Transforms text to uppercase.
3. LowerCasePipe: Transforms text to lowercase.
4. CurrencyPipe: Transforms a number into a currency string
5. DecimalPipe: Transforms a number into a string with a specified number of decimal places.
6. PercentPipe: Transforms a number into a percentage string.
7. JsonPipe: Converts a value into its JSON string representation.
8. SlicePipe: Creates a new array or string containing a subset of the elements.
9. AsyncPipe: Unwraps a value from an asynchronous primitive, such as a Promise or Observable.

Custom Pipes:

You can create your own custom pipes by implementing the PipeTransform interface. Here's an example of a custom pipe that capitalizes the first letter of each word in a string:

````typescript
import { Pipe, PipeTransform } from '@angular/core';
@Pipe({ name: 'capitalize' })
export class CapitalizePipe implements PipeTransform {
    transform(value: string): string {
        if (!value) return value;
        return value.replace(/\b\w/g, first => first.toUpperCase());
    }
    }
    ```
In this example, the `CapitalizePipe` takes a string input and transforms it by capitalizing the first letter of each word. You can use this pipe in your templates like this:

```html
<p>{{ 'hello world' | capitalize }}</p>
```This will output: "Hello World".
Pipes can also take parameters to further customize the transformation. For example, you can create a pipe that formats a number with a specified number of decimal places:


````

Types of pipes

1. Pure Pipes: are only executed when input value changes. they has no sideeffects. Angluar cache the output of pure pipes so they are re executed when the pipe chages. These pipes are stateless and do not depend on any external state. They only re-evaluate when the input data changes. Pure pipes are more efficient because they are only called when necessary.

2. Impure Pipes: they are executed on every change detection cycle, regardless of wheather the input value has changed. they has sideeffects. they are not chached by angular. These pipes can depend on external state and may re-evaluate more frequently, even if the input data has not changed. Impure pipes are less efficient and should be used with caution.
