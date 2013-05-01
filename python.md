#Print: Statement vs. Function in Python#

By Andrea Sassu, Eric Lobato, Jenaer Rader

#Python#

Python's goals as a language are:

- very clear, readable syntax
- 
- strong introspection capabilities
- 
- intuitive object orientation
- 
- natural expression of procedural code
- 
- full modularity, supporting hierarchical packages
- 
- etc...


Print as a statement does not follow these ideals.

#As a Statement#

Print is extremely straightforward and simple.

      print ("Print this line, and print a newline")
      print ("Print this line, but not a newline", end="")
      
#As a Statement#

      teeth = "white"
      coal = "black"

      print teeth,"teeth and",coal,"shoes"
      print teeth," - teeth and - ",coal," - shoes"

      teeth = "yellow"; coal = "red"
      print teeth,"teeth and",
      print coal,"shoes"

#As a Statement#

Print as a statement does not service complexity, however.
      
This print has unique syntax compared to other output methods, and is not as sophisticated.   

#Reasons for Change#

Print as a state was clunky and couldn't be entwined with other Python functions. It didn't meet Python's mission statement.

Python's Print was in Guido's "Python Regrets" presentation.

#Reasons for Change#

"There's no easy way to convert print statements into another call if one needs a different separator, not spaces, or none at all. Also, there's no easy way at all to conveniently print objects with some other separator than a space."

This exemplifies part of the power issue with print as a statement.

#Reasons for Change#

"Having special syntax for print puts up a much larger barrier for evolution, e.g. a hypothetical new printf() function is not too far fetched when it will coexist with a print() function."

This would make print more like printing in other languages, such as C.

#Reasons for Change#

If print() is a function, it would be much easier to replace it within one module (just def print(*args):...) or even throughout a program (e.g. by putting a different function in __builtin__.print).

Python can emulate something similar to this with write, but it is significantly more complicated.

#Reasons for Change#

Ideally, we want print to work equivilant to the following after this change:

          print(a, b, c, file=sys.stderr)

          print >>sys.stderr, a, b, c


#Print as a Function#

With Print as a Function, the syntax becomes more complicated, which allows for more complex and interesting output.

For example, you can make a seperator and end value to supress a new line.

#Print as a Function#

      basket = ('Apple', 'Oranges', 'Banana')
      print (*basket, sep=", ", end=".\n")

#Print as a Function#

      print (teeth,"teeth and",coal,"shoes")
      print (teeth,"teeth and",coal,"shoes",sep = " - ")

      teeth = "yellow"; coal = "red"
      print (teeth,"teeth and",end = "")
          
      print (coal,"shoes")
      
#Print as a Function#

You can use print inside a lambda,  a function call, etc.:

      example_timeout_function(call=lambda: 
          print('Hello world'), timeout=5)
      do_things(print_function=print)   
      
#Print as a Function#

You can use Print in ways as a function that you can't as a statement:

      [print(x) for x in range(10)]      

#Print as a Function#

Still allows for backwards compatability:

      >>> print ("Hello")
      Hello
      >>> print ("Hello", "world")
      Hello world

#Commuinity Response#

Generally, people liked the change, including Guido, and felt the changes made the overall feel of print morre suitable to their needs.

#Community Response#

One key positive: it feels more like Python.

__2.x:__

      print >> my_file, x
    
__3.x:__   

      print(x, file=my_file)

#Community Response#

The key downside: two extra characters.

__2.x:__

      print
    
__3.x:__   

      print()


#Conclusion#

Overall, this change was well desired, well implimented, and well recieved by the community.

__Print as Function > Print as Statement__
