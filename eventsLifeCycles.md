life cycle events.
Angular mein Lifecycle Events (ya Lifecycle Hooks) wo special methods hote hain jo component ki life ke different stages par automatically call hote hain.
Simple words mein:
👉 Jab component ban raha hota hai, update ho raha hota hai, ya destroy ho raha hota hai, tab Angular kuch specific functions run karta hai — inhi ko lifecycle hooks kehte hain.
hr component k apne life cycle events hota hai

jb bhi mera component initialize ho jae ge then ye life cycle events trigger ho jae ge

1.  ngOnInit
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

2. AfterViewInit
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

3. On destroy
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
