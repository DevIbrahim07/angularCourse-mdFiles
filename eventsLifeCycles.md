life cycle events.

lifeCycle hooks are the series of method taht angular calls at different stages of a component's life cycle. these hooks allow developers to execute specific code at specific moments in the component's life, such as when it is created, updated, or destroyed. By implementing these hooks, developers can manage resources, perform cleanup, and respond to changes in the component's state effectively.

Angular mein Lifecycle Events (ya Lifecycle Hooks) wo special methods hote hain jo component ki life ke different stages par automatically call hote hain.
Simple words mein:
👉 Jab component ban raha hota hai, update ho raha hota hai, ya destroy ho raha hota hai, tab Angular kuch specific functions run karta hai — inhi ko lifecycle hooks kehte hain.
hr component k apne life cycle events hota hai

ye 8 lifecycle events hote hain

1--ngOnChange: jb bhi component ke input properties change ho to ye event trigger hota hai
2--ngOnInit: jb component initialize ho jata hai to ye event trigger hota hai
3--ngDoCheck: jb bhi component ke data-bound properties change ho to ye event trigger hota hai
4--ngAfterContentInit: jb component ke content (ng-content) initialize ho jata hai to ye event trigger hota hai
5--ngAfterContentChecked: jb component ke content check ho jata hai to ye event trigger hota hai
6--ngAfterViewInit: jb component ke view initialize ho jata hai to ye event trigger hota hai
7--ngAfterViewChecked: jb component ke view check ho jata hai to ye event trigger hota hai
8--ngOnDestroy: jb component destroy ho jata hai to ye event trigger hota hai

1. ngOnChange example

export class Admin implements onChange{
constructor(){
// property initialization
}

        ngOnChange(changes: SimpleChanges): void{
            console.log("ngonchange"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

}

jb bhi mera component initialize ho jae ge then ye life cycle events trigger ho jae ge

2.  ngOnInit
    export class Admin implements onInit{
    constructor(){
    // property initialization
    }

        ngOninit(): void{
            console.log("ngonint"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

}

3 do check example

export class Admin implements onInit , DoCheck{
constructor(){
// property initialization
}

        ngOninit(): void{
            console.log("ngonint"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

        ngDoCheck(): void{
            console.log("docheck"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

}

4 AfterContentInit
jb component ke content (ng-content) initialize ho jata hai to ye event trigger hota hai
export class Admin implements onInit , AfterContentInit{
constructor(){
// property initialization
}

        ngOninit(): void{
            console.log("ngonint"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

    ngAfterContentInit(): void{
        console.log("aftercontentinit"   )
    }

}

5 AfterContentChecked
jb component ke content check ho jata hai to ye event trigger hota hai
export class Admin implements onInit , AfterContentChecked{
constructor(){
// property initialization
}

        ngOninit(): void{
            console.log("ngonint"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

    ngAfterContentChecked(): void{
        console.log("aftercontentchecked"   )
    }

}

6. AfterViewInit
   jb component mai sare view initialized ho jate hai then ye automatically triggered hota he

export class Admin implements onInit , AfterViewInit{
constructor(){
// property initialization
}

        ngOninit(): void{
            console.log("ngonint"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

    ngAfterViewInit(): void{
        console.log("afterviewinit"   )
    }

}

7 AfterViewChecked
jb component ke view check ho jata hai to ye event trigger hota hai
export class Admin implements onInit , AfterViewChecked{
constructor(){
// property initialization
}

        ngOninit(): void{
            console.log("ngonint"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

    ngAfterViewChecked(): void{
        console.log("afterviewchecked"   )
    }

}

8. On destroy
   component destroy hone se phle is mai likha hoa code run ho ga
   when we needed to navigate this will triggered

export class Admin implements onInit , AfterViewInit{
constructor(){
// property initialization
}

        ngOninit(): void{
            console.log("ngonint"  )

            here we can do
            // api call trigger krni he
            // subscription
        }

    ngAfterViewInit(): void{
        console.log("afterviewinit"   )
    }

    onDestroy():{
        console.log(" it is executed jb hamra component needs to be redirect to another page it will triggered")
    }

}
