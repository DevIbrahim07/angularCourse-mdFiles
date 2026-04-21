template are the html that angular renders for a component
Templates combine plain HTML with Angular template syntax to show data and react to user events.
template and templateUrl are the two ways to define a component's template.

# template

The template property hamai allow krta hai ki aap directly component ke andar hi HTML likh sakte hain.
@Component({
selector: 'app-hello',
template: `<h1>Hello, {{ name }}!</h1>`,
})
export class HelloComponent {
name = 'Angular';
}
is example mein, template property ke andar ek simple HTML string hai jo ek heading tag ko render karta hai. {{ name }} interpolation syntax ka use karke name variable ki value ko display kiya gaya hai.

# templateUrl

templateUrl property hamai allow krta hai ki aap apne component ke template ko ek
alag HTML file mein define kar sakte hain. Yeh approach zyada organized aur maintainable hota hai, especially jab aapke template mein complex HTML ho.
@Component({
selector: 'app-hello',
templateUrl: './hello.component.html',
})
export class HelloComponent {
name = 'Angular';
}
is example mein, templateUrl property ke andar ek path diya gaya hai jo hello.component.html file ko point karta hai. Aapko hello.component.html file create karni hogi aur usmein apna HTML likhna hoga, jaise:

<h1>Hello, {{ name }}!</h1>
{{ name }} interpolation syntax ka use karke name variable ki value ko display kiya gaya hai.
# Conclusion
template aur templateUrl dono hi Angular components ke liye templates define karne ke tarike hain. template property ke andar aap directly HTML likh sakte hain, jabki templateUrl property ke andar aap apne template ko ek alag HTML file mein define kar sakte hain. Aap apne project ki needs aur preferences ke hisaab se in dono mein se kisi bhi approach ka use kar sakte hain.
