## Key Word Cheatsheet

- ### **Function**
 - A function is a block of code (usually denoted by the word "function", or =>). This block of code will do be written in order to do something specific. For Example:
 `function getSomeSleep() { return "zzz..."}`
 - Above, we wrote the `getSomeSleep` function, but have not yet made it run.  It will only run once being invoked.
- ### **Invoke a function, Call a function, Execute a function**
 - Both *invoke*, *call* & *execute* when referring to a function means actually running the function. You can write a function, but it doesn't run until it has been invoked or called
 - A function can be invoked or called in numerous ways.  Most commonly thus far, we have seen functions called by writing the name of the function, and adding parenthesis: `getSomeSleep()` will run the `getSomeSleep` function, and return `"zzz..."`
- ### **Iterate, Loop**
 - You may hear the phrases "iterate over an array" or "loop through an array". These mean the same thing.  They both suggest that you need to write some sort of looping statement (like a for, while, forEach, map, etc.) to go from the beginning of the array through to the end, passing over each element. 
 - You can also use loops without an array.  Let's say you wanted to find every number divisible by 5 between 1 and 100:

 
~~~
for(let i = 0; i < 100; i++){
  if(i % 5 === 0) {
    console.log(`${i} is divisible by 5`);
  }
}
~~~

- ### **For Loop**
 - The for loop is one of the most essential building blocks in JavaScript.  It allows you to continue to run a certain block of code *over and over*, until you want that block of code to end.  In the example above, we wrote a for loop such that the value it began with was `i = 0`.  We wanted to run the block of code inside the for loop until `i = 100`, incrementing `i` by 1 each time. So, i will be 0, then 1, then 2, then 3, ... until it reaches 100.  When it finally reaches 100, `i < 100` is no longer true, so the loop ends!
- ### **While Loop**
 - Similar to the for loop, the while loop will also allow you to run a certain block of code *over and over*, until you want that block of code to end. 
 
 ~~~
 let x = 10;
 while(x > 5){
 	  console.log(x);
 	  x--
 }
 ~~~
  - As you can see in the above example, we will continue to console.log() out `x` until `x` is no longer greater than 5.  So, in the console, we will see 10, then 9, then 8, then 7, then 6. Note that we will *not* see 5, because 5 is not greater than 5!

- ### **If, Else If, and Else**
 - We use If statements to determine if something is true.  If that something is indeed true, the code will proceed to run whatever is inside of the if statement.  If not, it will move forward

 ~~~
 let name = "Alexander"
 if(name.length > 7){
       console.log("This is a long name!")
 }
 ~~~   
 
 - Above, the if statement will check the length of the name varialbe, and determine whether or not the length is greater than 7.  In this case, it is `(9 > 7 === true)`. So, we will see in the console `"This is a long name!"`

 - We can build off this logic, and add some *else if* logic in to this block of code! 

 ~~~
 let name = "James"
 if(name.length > 7){
       console.log("This is a long name!")
 } else if(name.length > 4){
       console.log("This name has a normal length.")
 }
 ~~~
 
 - Here, the if statement will check to see if name.length is greater than 7. `"James".length === 3`, so the `if` statement will *not* execute! Because the `if` statement didn't execute, the else if statement is next up.  The `else if` statement will now determine whether or not `"James".length` is greater than 4, and it is! Therefore, we will see in the console `"This name has a normal length."`.  Note that if we ran the name `"Alexander"` through this block of code, the `else if` statement would *never* run, because the `if` statement takes precedence.  Once the `if` statement runs (and finds truth, like "Alexander".length > 7), any subsequent `else if` or `else` statements will be ignored.

 - Finally, lets check out the else statement!  Going off our continued example, check out this block of code below:

 ~~~
 let name = "Bob"
 if(name.length > 7){
       console.log("This is a long name!")
 } else if(name.length > 4){
       console.log("This name has a normal length.")
 } else {
       console.log("This is a short name!")
 }
 ~~~
 
 - Here, the `if` statement would determine whether or not `name.length` is greater than 7.  It is not, so the code would then go to the `else if` statement to determine whether or not `name.length` is greater than 4.  The `else if` statement would also deduce that the statement is not true, which would take us to the `else` statement.
 - Notice that the `else` statement doesn't have any parenthesis after it?  That's because we are just using the `else` statement to capture *every other* possibility that didn't fall into the `if` or `else if`. 
 - Same as the `else if`, the `else` statement will never run if the `if` statement's parameters are truthy.  So, let's say `name = Alexander`.  The `if` statement would run, and then the `else if` and `else` statement would be completely ignored.

- ### **String**
 - A string is a data type that will always have some sort of quotes around it:
 - `"This is a string"`, `'so is this'`
- ### **Number**
 - A number is a data type that will always be numeric.  `4` is a number. `18.7` is a number.  `"25"` is a string.
- ### **True & False**
 -  `True and False` are what we call boolean values.  Ultimately, we will use truthiness and falsiness to determine whether or not we want to run particular lines of code (see if statements & loops)  
- ### **Object**
 - An object is a container.  It will contain data that can be accessed through key value pairs.  We store data inside of objects to keep things organized.

 ~~~
 let person = {
       name: "Alex",
       homeTowm: "Los Angeles",
       favoriteFood: "Tacos",
       age: 26,
       hungry: true, 
       pets: ["Romeo", "Winston", "Pinky", "Chloe"]
 }
 ~~~
 
 - Notice that inside this `person` object we have stored a bunch of data about a person named Alex! (me lol). Now, if I wanted to, I could have just stored all of those variables outside of the object: 

 ~~~
 let name = "Alex"
 let homeTowm = "Los Angeles"
 let favoriteFood = "Tacos"
 etc. etc. etc.
 ~~~
 
 - But what if we had multiple people and wanted to track all of their names, hometowns, favorite foods, and more?  It would get pretty messy trying to locate all of that information if it wasn't stored in data structures like objects. Each different person could have their own object, with the same keys `name, hometown, etc.`, but with different values!
 - To access information inside of this particular object, we could say something like `person.pets` to get the array of pets, or `person.favoriteFood` to get "Tacos"
    
- ### **Array**
 - An array is a specific kind of object.  It holds multiple values inside of it, but those values do not have key value pairs.  Instead, they are locaed by index.

 ~~~
 let pets = ["Romeo", "Winston", "Pinky", "Chloe"]
 pets[0] --> "Romeo"
 pets[3] --> "Chloe"
 ~~~
 - Much like objects, arrays can hold any kind of data that we want: 
 `let randomThings = ["hello", true, 17, "chicken", {hi: "bye"}]` 
 - In this example, notice `randomThings[4]` is an *object*! We can put *whatever we want* inside of arrays (and objects in general), which means that it's totally up to you how you'd like to structure them.
 
- ### **State**
 - In game logic, *state* represents the variables that will change throughout the course of the game.  State might hold information like the score, the turn, or the current positioning of pieces on a board.
- ### **Init**
 - In your game, the *init* function will be a function that your JS code should call as soon as the game loads in the browser, setting up all of the initial information for the game.  There is **nothing special** about the word "init".  We just call this function the "init" function because (if you write it properly) it will initialize everything in the game.  
 - In tic tac toe, we could initialize the `board` state variable to be an array containing 9 null elements `board = [null,null,null,null,null,null,null,null,null]`
- ### **Render**
 - The "render" function will be a function that your JS code should call every time there is an update to the state of the game. In your game, that will generally happen when a user interacts with the DOM.  For instance, when a user clicks on one of the squares in `tic-tac-toe`, that should run a function that changes your state in your JS file, and then renders the board such that it displays the new information.
 - Here's how that logic might flow in pseudo code:
 
~~~
If a player clicks on a valid square, run the handleClick 
function that has been passed into the addEventListener for the board

Determine which square was clicked on (e.target), 
and then determine which space in your board array (inside state) should 
be altered.  If the square in the center of the HTML board is 
clicked, you that should relate to the element with an index of 4 
in the board array. 

Determine which player clicked that element, and then update 
the board array such that it looks like this: 
board = [null,null,null,null,1,null,null,null,null]

(notice the "1" at board[4])

With this newly updated board array, we will need to update the HTML such that it represents the data properly.  We will have to iterate through the array, and interact with the HTML page such that it displays an "X" in the center of the board.
~~~    
