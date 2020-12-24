Recursive programming in Haskell
================================
Before we can talk about recursion, we need to discuss lists
 
A basic empty list can be written as []  
If x is some data and is followed by a list xs, it is written as x:xs  
A list [1,2,3,4] can be written as 1:(2:(3:(4:[]))), which can be written in a shorter form as 1:2:3:4:[]
 
Haskell is a language that encourages using as little parentheses as possible, so there are many cases where most languages would include parentheses, but Haskell allows developers to not have them, which increases the readability of the code. 
 
Haskell can break up these lists by using built-in commands such as head and tail.  
`head(1:2:3:4:[]) = 1`  
`tail(1:2:3:4:[]) = 2:3:4:[]`
 
Head returns the first element of the list, and tail returns a list containing every element after the head of the list.  
The len() function is the first function we will write in Haskell that uses recursion. Create a file called len.hs and write this into the file  
`len [] = 0`  
`len (x:xs) = 1 + len xs`
 
The way this works for our list defined above is like this:  
len 1:2:3:4:[] = 1 + len 2:3:4:[] -> 2 + len 3:4:[] -> 4 + len [] -> 4 + 0 -> 4
 
Another simple program that can be written in haskell is a function for the fibonacci sequence. Start by creating a file named fib.hs, and save this program into it  
`fib(0) = 1`  
`fib(1) = 1`  
`fib(n) = fib(n-1) + fib(n-2)`
 
Any value of n that gets input into this function will output you the fibonacci number of that order.  
A good place to read about recursion more is [here](http://learn.hfm.io/recursion.html)  
This is a solid article with great explanations and examples
