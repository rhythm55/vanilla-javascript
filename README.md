![Screenshot 2024-01-03 at 1 07 32 AM](https://github.com/rhythm55/vanilla-javascript/assets/36883992/9e41a863-8638-4e4d-9717-9ae114bc6976)# vanilla-javascript

### What is JS
    Dynamic: 
      With Js a lot of dynamic behaviour in website inertaction got inroduced like - pop ups . Earlier website used to reload in the window. 
    Interpreted: 
      Js is a interpreted language. that means its converted into machine code then excuted. Generally in our browser following steps take place by inbuilt         browser js engine -
        1. source code is parsed in js engine
        2. its converted into machine code
        3. machine code is executed
    Lossely typed:
      In Js there is not strict typing - a variable type can change during run time . Say you have a variable x assinged with numeric value. Same varialbe in later code can be assinged as string. This is generally not possible in other languages like - java, c++ etc.
      Hosted language:
        - Js can be run on browser, today most of the modern browser have JS engine in built like -
           - chrom v8
           - firefox SpiderMonkey
           in this case it do not have access to system variables etc. We get more visual interaction experience with it.
        - Js can also be run in system using node js
           after chrome v8 was launched it was converted as node js with which js can be executed in system.
![Screenshot 2023-09-16 at 2 27 15 AM](https://github.com/rhythm55/vanilla-javascript/assets/36883992/8b80b9bf-8d13-46b3-ab44-fcab60cba4c2)

***

### How do webpages works
![Screenshot 2023-09-17 at 6 18 18 PM](https://github.com/rhythm55/vanilla-javascript/assets/36883992/7fe1ec8a-839b-4f43-8684-5e7ac3241cef)

***

### Data types in JS

#### Primitive 
    The predefined data types provided by JavaScript language are also known as in-built data types.
    Number, String, Boolean, Null, Undefined

#### Non-Primitive
    Derived data types or reference data types i.e we refer to an address in memory
    Object, Array, Function, Date, Regx
![js-datatype](https://github.com/rhythm55/vanilla-javascript/assets/36883992/fb65304c-7f10-4f55-88c2-e77f92e148c0)

#### Converting data type
    PareseInt (Number without decimal values), ParseFloat(numbers with decimal places), toString()

***

### Variables in JS

#### What are variables
    variables are data containers that stores a data
    we have two ways of declaring variables using let and const

##### let
    it can be re intialized
    does not needs to be initialized at the time of the declaration
    used when variable value will be changed in program lifecycle
##### const
    it cannot be re intialized
    needs to be initialized at the time of the declaration
    used when variable value will remian same in program lifecycle

#### Shadowed Variable
    if we declare two variables in different scopes - local and global its allowed in JS. Not allowed in same scope.
    Reason - variable declared in global will be available in global scope. the one created in local scope will have different declaration then global scope.
    for ex:
        
                let userName;

                function nameChange(){
                   let userName = "rhythm thakur";
                   console.log(userName);  
                }
                userName = "rhythm";
                nameChange(); // output will be rhythm thakur - here local scope was considered for userName - also known as Shadowed variable
                console.log(userName); // output will be rhythm
***

### Operators
#### Mixing Numbers & Strings
    - `+` operator also support strings.
        3 + 'hello' // outpur is 3hello
    - other operators dont support string but they are able to smartly convert string number to number for operations
        3 - 'hello' // NaN
        3 - '3' // 0
        2 * 'hi' // NaN
        2 * '2' // 4
#### a++ vs ++a 
    ++a returns value after update
    a++ returns value before update
    example - 
        const a = 1;
        console.log(++a); //2

        const a = 1;
       console.log(a++); //1

#### Operator precedence

    () > Increment Operators(++,--) > NOT Operators(!,~) > Arithmetic Operators(*,/,% > +,-) > Comparison Operators > Logical Operators

***
### Null / Undefined / NaN

#### Undefined
    Data type. 
    When a variable is defined in JS without initializing any value by default its assigned with undefined.
    We should not assign undefined manually not a good practice.
    Example
        let a;
        console.log(a); //undefined
    
#### Null
    Special value
    Data type of null is Object.
    Can be used when we want to reset value of a variable.
    
#### NaN
    Not a Number
    Its a number that is not a legal number
    Its usually comes into picture when we have invalid number calculations
    example:
        console.log(3*'hi"); //NaN

***

### Importing script with async and defer
    Both are only applicable to external scripts - as with internal there is nothing to download.
![Screenshot 2023-09-27 at 2 07 35 AM](https://github.com/rhythm55/vanilla-javascript/assets/36883992/e8413166-c179-4e53-9439-a279045309fa)

#### Defer
    When we want to load the script and execute after HTML is parsed.
    This saves time of loading while html is parsed.
    Usually used to improve performance and when we want the script only to be executed once HTML is parsed.
    
#### Async
    When we want to load script as soon as it loads.
    If it load while html parsing is in progress - once the loading of script is done html parsing will be paused to execute the script once execution is done html parsing will be resumed.
    Usually used when we want script to be loaded first.
    
***

### Falsy and Truthy Values
    JavaScript is able to use variables in conditions - even without comparison operators. When it sees a variable in a condition it automatically coerce ("convert without really converting") the values you pass to if .
![Screenshot 2024-01-03 at 1 07 32 AM](https://github.com/rhythm55/vanilla-javascript/assets/36883992/d59c7095-8e2e-483b-a025-edae555f2655)

***

### Boolean tricks
![Screenshot 2024-01-03 at 1 47 32 AM](https://github.com/rhythm55/vanilla-javascript/assets/36883992/4a4891b2-2036-4cf7-9383-3aef4b13f3cd)

***

### For loops in JS
![Screenshot 2024-01-03 at 1 55 05 AM](https://github.com/rhythm55/vanilla-javascript/assets/36883992/8b0bfd98-54af-4e6e-ad73-e16c612d6540)

***

### Primitive vs Refrence Value
![Screenshot 2024-01-03 at 11 43 19 PM](https://github.com/rhythm55/vanilla-javascript/assets/36883992/77213722-6019-43d5-ae8c-5de5e5abbe15)

    Objects are refrence values that is why we cant compare equality using === or == . consider below example -
    const a = {age: 30}
    const b = {age: 30}
    console.log(a == b) // this will return false 
    reason : a and b are storing a refrence and equality is checking the address which is why it will always be false

    Array are refrence values . Check below example 
    const a = ['apple']
    a.push('grapes') // const can not be changed so it should throw an error - but here it wont
    reason: here error wont be thrown because const is storing refrence address which is still same - the value to which refrence pointing to is changed

