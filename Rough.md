Rough Draft
===========

###Introduction###

Python is a powerful, dynamic programming language designed to be extremely easy to learn and user-friendly. 
It is an extremely flexible language. It boats its good use of speed, friendliness with other languages, and especially it's easy readbility. 
The syntax of Python is likely it's more notabile characteristic, which has made it a very well-liked language 
throughout the software community. However, one of "Python's Great Regrets" was its implimentation of the print function. 
The creators or Python made print as a statement, a simple line of code to execute, but with little power compared to what old programmers would expect such an action to have.
This has caused the community to propose making print a function in 2006, which has since been accepted and impleented since Python 3.0. This paper shall analyze the process, reasoning, and changes that occur with this change.

###Print as a Statement###

Statements in Python are simple lines of code. Considering print, it simply consisted of a few arguments, as seen below:

          print ("Print this line, and print a newline")
          print ("Print this line, but not a newline", end="")

Each new line of code needs a new print statement, if the statements are compelx enough to require multiple executions. 
The outputted content must be put within quotaion marks. If the programmer wants to output the value of a variable, then that must not be in quotes.
Different content, like switching between text and variables, must have commas between the items in order for the compiler
to understand the different arguments. This is exemplified below:

          teeth = "white"
          coal = "black"

          print teeth,"teeth and",coal,"shoes"
          print teeth," - teeth and - ",coal," - shoes"

          teeth = "yellow"; coal = "red"
          print teeth,"teeth and",
          print coal,"shoes"
          
This impliementation is extremely straightforward. Statements have the benefit of being easy to read and execute, because the symtax is still straightforward.
However, this is also the great flaw of print as a statement: it can do little more than what is seen above. 
Print has issues being combined with other functions, and must not occur within another function. This is not nearly as powerful 
as the print function in C or C++, for example, which has the ability to be used almost anywhere in the code. Python users wanted 
be able to use this sort of power in their Python code, which helped inspire the proposal to change print from a statement to a function.

###Reasons for Change###
