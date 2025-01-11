ref: [1]https://docs.python.org/3/tutorial/controlflow.html#defining-functions

method: a function that belongs to an object. Different types define different methods. you can create methods and data types using classes.

specifying default values allows you to create a function that can be called with fewer arguments that is defined to allow

default values (parameters like x=1) are evaluated at the point of function definion in the defining scope (meaning functions will hold values that the parameters are assigned to based on what they were defined at the scope when the function was defined)

you can modify mutable objects though. like if you had a default value as a list for example you can add or remove from it.

as long as you have default values as parameters, you can use them in any order as arguments according to the rules of [1]4.9.2



1. print statement will send the string to the console
return will store the value but not necessarily send that value to the console. that value would then be stored in a variable or some other object for later use.
2. 
	1. function definition: the function at the point which you create it
	2. function call: running the function. 
4. You use a return statement when you want to store a value for later use
1. you use a print statement when you just want to display a message to the console
2. function parameters are variables scoped to the function they belong to that are used as aliases to the arguments that are given when the function is called.