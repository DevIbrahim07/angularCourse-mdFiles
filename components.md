Components are the main building blocks of Angular applications. Each component represents a part of a larger web page. Organizing an application into components helps provide structure to your project, clearly separating code into specific parts that are easy to maintain and grow over time.

hr component ka aik unique name hota he . jis ki basis pr hm usee dusre components mai load / use krte hai . we can call it selector .
and use it like an html tag <app-admin  ></app-admin>

also phle we import it in ts file of component where we are going to use it .

@component{
selector: "app-admin"  
}

.. decorator tells angular what type of class is this
/ ye decorator he  
@Component({
selector: 'app-user',
imports: [],
templateUrl: './user.html',
styleUrl: './user.css',
})
export class User {} // class but nothig

// now agr hm aik component mai styling krte hai us ki css file mai . to wo dusre components ko access nai ho skti styling . if we want to apply same styling to other compoents as well we use it in global css. style.css file mai
