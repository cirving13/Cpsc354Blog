Lean
====
Lean is a programming language that is designed to prove theorems by using automated tools and methods, as well as user interaction and the construction and development of a 
complete proof. It is also known as a proof assistant, which is software that provides a language for defining objects, specifying properties of those objects, as well as proving that those specifications do hold. 

mathlib
=======
mathlib is a community driven library that contains mathematics that is formalized into the Lean proof assistant. The library is overseen by Microsoft Research, however all entries 
and definitions that are added into the library are primarily from contributors with a passion for the advancement of mathematics, as well as the development of their potential in developing the proof assistant side of Lean. A brief overview of the mathlib can be found [here](https://leanprover-community.github.io/mathlib-overview.html). This has a rough list containing the topics and definitions that are currently covered in mathlib. Anyone is allowed to make updates to the list by creating their own branch of the mathlib and writing and testing their new methods and definitions. And when you have created something and tested it to its entirety, you can create a merge request, in which a small group of people will examine and test your code, to determine whether it is approved to be added to the library. 

Different Modes
===============
Lean is equipped with different modes to aid in different aspects of the programs uses.  

Tactic Mode
-----------
Anywhere were an expression is expected, lean will accept a sequence of instructions between a `begin` and an `end`. The sequence of inputs between the begin and end is known as a tactic and is usually separated by commas. Lean will execute the tactic expecting it to create an expression of the required type at the output. The results from these tactics are checked by the kernel, and there can be other tactics that are used to catch or handle these failed tactics. If the error is not handled, an error message will be provided to the user. Tactics will not succeed if they do not produce the required type that is needed for the function to run.  

Calc mode
---------
Calc mode is an environment that is used to complete calculations and write Calculational proofs. This is written as a chain of intermediate results that are composed together to form a larger proof. To enter calc mode, simply place `calc` before a line that you want computed in a calculation environment.  

Conv mode 
---------
While inside a tactic block, you can use the keyword `conv` to enter conversion mode. In conversion mode, you are able to travel inside the assumptions and goals of the tactics written.  

Simp tactic
-----------
Simp tactic stands for Simplifier tactic. This is ran as the last tactic in a sequence and is used to try and simplify your goal at the end of your tactic sequence. Simp is equipped with a list of lemmas that attempt to match subterms of the goal with left side rules and match them to right side rules. This set of lemmas will set out to try and prove your goal, you can also add to your simp lemmas to add extra lemmas to be used in your proving. 
