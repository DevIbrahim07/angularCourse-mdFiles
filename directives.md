Directives are classes that add additional behavior to elements in your Angular applications. They are used to manipulate the DOM, handle events, and create reusable components. There are three types of directives in Angular:

Types of Directives

1. Component Directives: These are the most common type of directives and are used to create reusable components. They have a template and can include other directives.
2. Structural Directives: These directives change the structure of the DOM by adding or removing elements
3. Attribute Directives: These directives change the appearance or behavior of an element, component, or another directive.
   Creating a Directive
   To create a directive, you can use the Angular CLI command:

```bash
ng generate directive directive-name
```

This will create a new directive file with the necessary boilerplate code. You can then modify the directive to suit your needs.

1--component directives
they are used with a template . it define angular component.

2--structural directives
they are used to change the structure of the DOM by adding or removing elements. They are denoted by an asterisk (\*) before the directive name. Examples include @If, @For, and @Switch.

@if is used to conditionally include or exclude an element from the DOM based on a boolean expression.
@For is used to repeat a template for each item in a collection. It takes an iterable expression and creates a new instance of the template for each item.
@Switch is used to display different templates based on a switch expression. It works together with @

3--attribute directives
they are used to change the appearance or behavior of an element, component, or another directive. They are denoted by the absence of an asterisk (\*) before the directive name. Examples include @Class, @Style, and @Model.
@Class is used to add or remove CSS classes from an element based on a condition.
@Style is used to set inline styles on an element based on a condition.
@Model is used to create a two-way data binding between an input element and a property in the component. It allows you to update the property in the component when the user types in the input field, and vice versa.

Custom Directives
In addition to the built-in directives, you can also create your own custom directives to add specific behavior to your application. To create a custom directive, you need to define a class and decorate it with the @Directive decorator. You can then implement the desired behavior in the directive's class.

an example of a custom directive that changes the background color of an element when the mouse hovers over it:

````typescript
import { Directive, ElementRef, HostListener } from '@angular/core';
@Directive({
  selector: '[appHoverHighlight]'
})
export class HoverHighlightDirective {
  constructor(private el: ElementRef) {}
  @HostListener('mouseenter') onMouseEnter() {
    this.highlight('yellow');
  }
  @HostListener('mouseleave') onMouseLeave() {
    this.highlight(null);
  }
  private highlight(color: string) {
    this.el.nativeElement.style.backgroundColor = color;
  }
}
```In this example, the `HoverHighlightDirective` listens for mouse enter and leave events on the host element. When the mouse enters, it changes the background color to yellow, and when the mouse leaves, it resets the background color.To use this directive in your template, you can simply add the `appHoverHighlight` attribute to any element:```html
<div appHoverHighlight>Hover over me to see the highlight!</div>
```This will apply the hover highlight behavior to the div element. You can customize the directive further by adding input properties or handling additional events as needed.


````
