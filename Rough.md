Rough Draft
===========

###Introduction###

Python is a powerful, dynamic programming language designed to be extremely easy to learn and user-friendly. 
It is an extremely flexible language. It boats its good use of speed, friendliness with other languages, and
especially it's easy readability. The syntax of Python is likely it's more notable characteristic, which has made 
it a very well-liked language throughout the software community. However, one of "Python's Great Regrets" was its 
implementation of the print function. The creators or Python made print as a statement, a simple line of code to
execute, but with little power compared to what old programmers would expect such an action to have. This has caused 
the community to propose making print a function in 2006, which has since been accepted and implemented since 
Python 3.0. This paper shall analyze the process, reasoning, and changes that occur with this change.

###Print as a Statement###

Statements in Python are simple lines of code. Considering print, it simply consisted of a few arguments, as seen below:

      print ("Print this line, and print a newline")
      print ("Print this line, but not a newline", end="")

Each new line of code needs a new print statement, if the statements are complex enough to require multiple executions. 
The outputted content must be put within quotation marks. If the programmer wants to output the value of a variable,
then that must not be in quotes. Different content, like switching between text and variables, must have commas 
between the items in order for the compiler to understand the different arguments. This is exemplified below:

      teeth = "white"
      coal = "black"

      print teeth,"teeth and",coal,"shoes"
      print teeth," - teeth and - ",coal," - shoes"

      teeth = "yellow"; coal = "red"
      print teeth,"teeth and",
      print coal,"shoes"

This implementation is extremely straightforward. Statements have the benefit of being easy to read and execute, 
because the syntax is still straightforward. However, this is also the great flaw of print as a statement: it can 
do little more than what is seen above. Print has issues being combined with other functions, and must not occur 
within another function. This is not nearly as powerful as the print function in C or C++, for example, which has the 
ability to be used almost anywhere in the code. Python users wanted be able to use this sort of power in their 
Python code, which helped inspire the proposal to change print from a statement to a function.

###Reasons to Change###

The key reasons for change come from Grudio's presentation on his regrets on Python as a language, thus further
helping identify the real issues with print as a statement even from the creator's perspective.
To quote the official Python Evolution Proposal, "If print() is a function, it would be much easier to replace it within 
one module (just def print(*args):...) or even throughout a program." This would allow for much more widespread use 
throughout the code, and also make it easier to evolve the function. Versatility is extremely important for this portion of the 
language, which is one of the key ways it can output information to the user. Also, "print is the only application-level 
functionality that has a statement dedicated to it. Within Python's world, syntax is generally used as a last resort, 
when something can't be done without help from the compiler. Print doesn't qualify for such an exception." Making this change 
keeps more true to the nature and goals of the Python language.

Overall, the goal to change the print to a function will make it similar to the following sort of execution below:

          print >>sys.stderr, a, b, c
          
(Continue analysis given from official PEP)

###Print as a Function###

Functions in Python are the backbone of the programming language. They must be powerful enough to function well on their own, 
but also flexible enough to be combined with plenty of other functions. Print is no such exception. An example of the 
new implementation of print after Python 3.0 is as follows:

          basket = ('Apple', 'Oranges', 'Banana')
          print (*basket, sep=", ", end=".\n")
          
The syntax of a function is more complicated than that of a statement, which makes it a bit more difficult to read 
and program for new programmers. It is much less intuitive to have to include an extra seperator value to the print statement, 
for example, which can made this particular segment of code harder to read.

However, this syntax allows for much more powerful outputs. The code below is the same as what is expressed in statements 
above, but now the print is used as it would be in Python 3.0 and onward, with print as a function:

          teeth = "white"
          coal = "black"

          # print is a function
          # You can supply a sep value as the separator
          # You can supply an end value to supress new line

          print (teeth,"teeth and",coal,"shoes")
          print (teeth,"teeth and",coal,"shoes",sep = " - ")

          teeth = "yellow"; coal = "red"
          print (teeth,"teeth and",end = "")
          
          print (coal,"shoes")
          
###Community Response###

The community response to this change was generally positive. Print was made similar to other language's versions of 
printing output, which allows for well seasoned programmers to utilize print in a way that they feel is both familiar 
and accomidating enough for what they expect. Print can be used with any other function and more flexibly in the code, 
which is better in line with what software developers would hope fore.

For people who are new to programming and come to Python, the print statement can still be made as a friendly function. 
The implementation methods used while print was a statement still work for print as a function; that is, simply putting words 
in the double quotation marks yields a simple print statement, so there is backwards compatibility for easier-thinking programmers. 
Overall, this change makes print ore accessable for all types of programmers in the Python community, which is why 
the move was made without many complications of complaints from the community.

###Conclusion###

The decision to move print from a statement to a function was overall a good idea. The community has since felt that print can now 
meet its more complicated demands when necessary without being overly complicated for the new users. The power and funcationality 
of the new print since Python 3.0 fits in much better with Python's feel as a language, as it still is simple, fast, and powerful. 
