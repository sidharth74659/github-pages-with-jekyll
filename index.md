
# Everything about Variables in Javascript 



I'm glad you are here. I plan to talk about variables...


Let's look at basic syntax of how we declare variables : 
```JavaScript
// syntax:
variable variableName = DataType;
```

DataType could be a number, string, boolean, and [more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)


Let us look at how we can name variable names first :
```JavaScript

//  variableNames : 

    // You cannot use a JavaScript keyword as a variable name
    var var = "Google for keywords in JavaScript";   //invalid

    //can use numbers but cannot initiate a variable name with it
    const number4 = 4;    //valid
    const 4  = "four";    //invalid
    const 7number = 7;    //invalid

    // _ and $ can be used anywhere in variable name
    const _number1 = 8;  
    let $array_1 = [1, "string", true];    

    //variable names are case-sensitive
    let dev = "hello";
    let Dev = "dev"; //dev and Dev are different

    //using camelCase format makes your code look
    //clean and understandable 
    let isBoolean = true;  


//Note: Just because you can name variables in these formats, doesn't mean you should, google for "naming conventions" and follow something that you prefer...It helps in writing clean code and helps other devs(mostly yourself) to understand the code.
```

Few terms to know before we start defining variables:

  ..* Scope is a term used to mention that the code is inside the {brackets}

 ..* block-scope: code that is inside the function, for-loop, if-else statements, anywhere that lives inside {brackets}

  ..* function-scope: code that lives INSIDE the function {brackets} only


Ok. Let's start 

You can use `var`, `let`, and `const` to declare a variable...

```JavaScript
// sample code : 
var number = 4;
let string = "four";
const bool = true; 
```

`var`: 

>can be modified: it means you can modify the variable's value after declaring once. You don't need to mention the type of variable again

```Javascript
var age = 10;
age = 25;

console.log(age)    //OUTPUT : 25
```

> function-scoped: it means variables declared inside a function are not accessible outside the function scope...


```JavaScript
//var is function scoped

var greet = "Hello Dev";
console.log(greet); // OUTPUT : Hello Dev

function funName() {
    var note = "you can't see me";
    var greet = "greet updated";

    console.log(note);  //OUTPUT : you can't see me
    console.log(greet); //OUTPUT : greet updated
}

funName()

console.log(note);  //Error : note is not defined

console.log(greet);  //OUTPUT : Hello Dev
```

>are not block-scoped : it means variables declared inside {} (such as loops) are accessible outside 
```JavaScript
for (var i = 0; i <= 1; i++) {
    var block = "{} are called blocks"
    console.log(i)
}

console.log(block)  //{} are called blocks
```
```JavaScript
var number = 10;

if (number = 10) {
    number = 15;
}

console.log(number) //15
```

If you liked this so far, let me know..I'm in twitter @Srikanth74659 and i'll be glad to tell you more about `let` and `const`

Thank you for reading so far.
