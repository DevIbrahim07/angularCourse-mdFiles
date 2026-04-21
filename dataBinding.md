data binding aik process hai jisme hum apne component ke variables ko html ke elements se connect karte hai . isse hum apne data ko dynamically update kar sakte hai aur user ke interactions ke hisab se changes dekh sakte hai .

types of data binding in angular :
One way data binding > interpolation , property binding, event binding
Two way data binding > ngModel

interpoloation > interpolation ka use hum apne component ke variables ko html ke elements me display karne ke liye karte hai . isme hum double curly braces {{}} ka use karte hai .

property binding > property binding ka use hum apne component ke variables ko html ke properties se bind karne ke liye karte hai . isme hum square brackets [] ka use karte hai .

event binding > event binding ka use hum apne component ke variables ko html ke events se bind karne ke liye karte hai . isme hum parentheses () ka use karte hai .

ngModel > ngModel ka use hum apne component ke variables ko html ke form elements se bind karne ke liye karte hai . isme hum [(ngModel)] ka use karte hai .

class Admin {

    course: string = " angular course"

    consrtuctor(){
        console.log(
            this.course
        )
    }

    this.course = " angular new course"
    console.log(this.course)

}

when we create / declear a new variable in a component cannot acceesable to another component html .

1. interpolation > {{}}
2. property binding > HTML property ko JS variable se bind karna

3. ngModel > [(ngModel)] sync mai rakhta he .
4. event binding >
