Exceptions in Haskell
=====================
An exception is an event that happens while executing a program that breaks the flow of instructions. Haskell does not have built-in exception handling, so you need to use the `import Control.Exception` at the top of your .hs file if you plan on handling exceptions. 

To define your own exceptions, it should be written as  
`data myError = errorA | errorB deriving Show`

This line above is how a function would throw the error, to catch some error, we need to write a catch function:  
`catch :: Exception e => IO a -> (e-> IO a) -> IO a`  
This gets an IO action, in this case being some handler function, and produces some new IO monad. To call catch, we need to run  
`catch ioAction exceptionHandler`  

A full example of how catching an error would be written is shown here,  
``import Control.Exception  
data myError = Error deriving Show  
instance Exception myError  
failing :: IO ()  
failing = do  
  throw Error  
main :: IO ()  
main = do  
  catch failing (\e :: myError) -> do  
  putStrLn "Something is broken"``
  
To read more about exceptions, as well as built in exceptions in the Control.Exceptions package, visit [here](https://hackage.haskell.org/package/base-4.12.0.0/docs/Control-Exception.html) or [here](https://wiki.haskell.org/Handling_errors_in_Haskell)
