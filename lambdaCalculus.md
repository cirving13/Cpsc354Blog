Lambda Calculus
===============
Lambda calculus has 3 programming constructs, Abstraction, Application, and Variables. 
Abstraction: this is read as a program e with a parameter x. However abstraction allows us to abstract out the x, because the program does not depend on x now.  
&#955;x.e  
Application: if a and e are programs, then ae is a program that applies function a to the argument of e.  
Variables: Treated as normal variables, no special way of writing a variable either

A program of plus one would be written like this  
`int plusone(int n) {return n+1}`  
This can be written in &#955;-Calculus form like so  
`(&#955;n.n+1)x`  
Where x is some input that would be plugged into the equation.  

Dropping Parentheses
====================
There are many situations where the inclusion of parentheses makes a lambda Calculus equation difficult to read and interpret, we want to minimize the use of parentheses as much as possible. For this section, I will use arrows to show the simplification of certain equations:  
((ab)c)->(abc)->abc  
(((ab)c)d)->((abc)d)->(abcd)->abcd  
(&#955;x.(&#955;y.(&#955;z.e)))->&#955;x.&#955;y.&#955;z.e  
There are some parentheses that cannot be removed, like (a(bc)) can be reduced to a(bc) but cannot be reduced further to abc. These will depend on the individual program and what the inputs are for it. 

An excellent site to learn more about lambda Calculus is [here](https://plato.stanford.edu/entries/lambda-calculus/). It is an eBook from Stanford and discusses everything from the applications, to reduction to even the history behind lambda calculus as a whole. 
