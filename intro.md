Welcome to my Haskell Blog
==========================
Haskell is a statically typed, purely functional programming language that has been used to create advanced programming language features, including type-classes. This semester, I used Haskell in my programming languages class, and we used it to design our own programming language, with unique syntax, to help us learn about the inner-workings of a programming language and how they may be written and developed.
 
Before you can do any development with Haskell, you must install it, you can head to this [link](https://get-ghcup.haskell.org) for some other methods of installation, but this is what I did for installing on my Macbook
 
You are going to want to cd into the location in which you want these files to be installed, then download ghcup by running this command in the terminal:  
`curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh`
 
this installs ghcup onto the computer, as well as happy and alex, in the event it does not install the latter two programs, run these commands in your terminal  
`cabal install happy`and  
`cabal install alex`
 
then you want to install bnfc. the way i did it was run the command  
`cabal install BNFC`
 
but the commands:  
`git clone https://github.com/BNFC/bnfc`  
`brew install make`  
Should work fine as well.
 
You then need to cd into bnfc and run make. If you do not have make, then run  
`xcode-select --install`
This should install most of your command line utilities and set them up for you if you are on mac. Installing haskell on windows has a different set of steps, but I have not spent much time programming on a windows machine so I cannot speak on the matter. You should now be able to use bnfc and Haskell on your machine. You can test if it is on your machine by running bnfc --version and you should get a version of 2.8.3 or higher (if there is a newer version by this point) 
