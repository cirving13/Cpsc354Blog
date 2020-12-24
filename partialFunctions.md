Partial Functions
=================
A partial function is a function that is not defined for all possible arguments of some type.  
Examples of these functions were discussed earlier, the head and tail functions are undefined for empty lists. The divide function div is undefined if the divisor is 0, making it another partial function.  

Applying Partial Functions
==========================
Calling a function with multiple parameters, without calling all of the parameters is called applying a partial function. Let a function add be written as below  
`let add x y = x + y`  
We can call add in a function for add, to add a value by a set number of 2, like so  
`let a = add 2`  
`let b = a 4`  
b would be equal to 6 here, because a 4 is interpreted as `add 2 4`  
While partial functions work in its entirety, It is easier to read, develop, interpret, and is more complete. It also helps avoid the states where your code will compile, but not be successful in the end. 

Avoiding Partial Functions
==========================
There are a handful of functions in the Haskell Library that are partial functions and can be dangerous to your code and cause countless problems with matching data types and other things as well. One way to avoid this is by using functions from the [safe](https://hackage.haskell.org/package/safe) library instead, or writing your own functions to adapt them to complete functions.  
An example to this would be adding a case for the head and tail function that would account for an empty list. Here is a [link](https://wiki.haskell.org/Avoiding_partial_functions) that talks about avoiding partial functions
I will list some extra links here to read more about Partial functions and their applications  
[Partial application](https://wiki.haskell.org/Partial_application)  
[Partial functions](https://wiki.haskell.org/Partial_functions)  
[partial function application](https://blog.carbonfive.com/partial-function-application-in-haskell/)  
