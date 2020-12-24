Modules in Haskell
=================
A module is a collection of related functions, types and typeclasses. A Haskell program is a set of modules where one module uses the other modules together to complete some task given. Splitting up code into modules allows for more applications in your program, better flexibility, and prevents writing duplicate code. Generic modules are modules that are used accross numerous different programs. The ability to split your code into modules that do not have to rely on eachother to work allows you to reuse those modules in other programs or in other parts of the current program.  

To import a module, you simply want to type `import <module name>` at the top of your file, and you will have access to everything contained in that module. 

if you use the "as" keyword, it will rename the module as something else:  
`import Module as name`  
This allows you to use modules that have long or annoying names and make them something a little simpler. 

the "qualified" keyword forces you to put the name of the module in front of the name of the function whenever it is called in the program. This is helpful if you are importing modules which contain functions of the same name.  
```
import qualified ModuleName
ModuleName.FunctionName 
```
Here is how you would call a function from "ModuleName" while using the qualified keyword.  

Defining Your Own Modules
-------------------------
To create your own module, you are going to need to have a new file that has the same name as your module. You can only have one module per file, because importing a module is importing the entire file, and not just some module that is located in the file.   
`Module name = FileName --in FileName.hs`

If you are trying to call a module that is in a directory, you can call it by placing a "." between the directory name and the file name. For a file "Bar.hs" in a directory of "Foo", we can call it like so  
`import Foo.Bar`  

For more information on modules, visit the [Haskell Documentation](https://www.haskell.org/onlinereport/modules.html). This is somewhat hard to read, so another good source is this [book](http://learnyouahaskell.com/modules).
