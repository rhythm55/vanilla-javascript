# vanilla-javascript

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

####Primitive 
    The predefined data types provided by JavaScript language are also known as in-built data types.
    Number, String, Boolean, Null, Undefined

####Non-Primitive
    Derived data types or reference data types i.e we refer to an address in memory
    Object, Array, Function, Date, Regx
    ![js-datatype](https://github.com/rhythm55/vanilla-javascript/assets/36883992/fb65304c-7f10-4f55-88c2-e77f92e148c0)

### Variables in JS

    ####What are variables
        variables are data containers that stores a data
        we have two ways of declaring variables using let and const

        #####let
            it can be re intialized
            does not needs to be initialized at the time of the declaration
            used when variable value will be changed in program lifecycle
        #####const
            it cannot be re intialized
            needs to be initialized at the time of the declaration
            used when variable value will remian same in program lifecycle

    #####Shadowed Variable
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
