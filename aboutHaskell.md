About Haskell
=============
Haskell is a statically typed, general purpose, purely functional programming language with type inference and lazy evaluation. This post will discuss what each of these things mean and how they apply to Haskell

Statically Typed
================
A language is statically typed if the type of the variable is defined at compile time, as opposed to run time. This checks variables at compile time and will not compile a program if there is an error within it involving variables. 

General Purpose
===============
A language that is described as "General Purpose" is a language that can be used for anything. These languages have a wide range for application and are not confided to having some special purpose, also known as a domain-specific language. An example of this is SQL which is designed to manipulate databases.

Purely Functional
=================
A purely functional programming language is one that has a designated style of building elements of the programs. This treats all computation done by a program similar to a mathematical function. This is why Haskell has no assignment, and instead has `=` read as an equality symbol. 

Type Inference
==============
Type Inference is the ability of a language to automatically detect the type of some expression being used in the programming language. This allows the developer to not have to specify the type such as int 1 and instead just write 1. 

Lazy Evaluation
===============
Lazy Evaluation does not compute or evaluate an expression until it is called. This allows values to only be created when they are called upon, saving memory and reducing runtime. This also allows the ability to use structures as abstractions instead of primitives, as well as have a more straightforward implementation of certain algorithms. The disadvantages to lazy evaluation include being difficult to implement features such as exception handling, and can cause memory leaks and cause additional issues in your code because of it. Most of the time, a program that has Lazy evaluation, is also statically typed. These two build off of eachother and many properties of a statically typed language overlap with one with lazy evaluation. This was actually created for Lambda calculus, which is discussed [here](https://github.com/cirving13/cpsc354blog/edit/main/lambdaCalculus.md) 
