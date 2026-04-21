variable creation and data binding
primitive data types in ts
string , number, boolean, date

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
