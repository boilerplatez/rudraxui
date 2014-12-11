# Sample Module
Lets create a sample module ModuleA.
```
utils.define('ModuleA').as(function(ModuleA,_instance_){

    var PRIVATE_MODULE_VARIABLE = "I AM HIDDEN";

    ModuleA.PUBLIC_MODULE_VARIABLE = "I AM MODULE VARIABLE";

    ModuleA.say_hello = function(){
        alert('Hello all');
    };

    _instance_.sayHi = function(){
        alert('Hi all, I am instance of type ModuleA');
    };

})

```
Now what is happening in this code? If you are familiar with OOPS, then thats it. Any module can be defined using 'utils.define'. There are two methods defined in the above code.

Both are accessible publically, but one is linked with Module definition and other is with it instance.


```
var MyLocalModuleReference = utils.module('ModuleA');

//Now I can use 'say_hello' method
MyLocalModuleReference.say_hello();

//We can access Module Vaiables
alert(MyLocalModuleReference.PUBLIC_MODULE_VARIABLE)

//PRIVATE_MODULE_VARIABLE cannot be accessed outside definition

//Lets create an instance of this module
var myModuleInstance = MyLocalModuleReference.instance();

//Now I can use sayHi method
myModuleInstance.sayHi();
```

Hey still there or left? If you there then you might have one of these questions in your mind : -

1. What is this?
2. Why are we dong this?


Answers are :-
1. Leave it, its not your cup of tea, do what you do best.
2. Well you will know. Keep reading.

