##In 2.x

          print ("Print this line, and print a newline")
          print ("Print this line, but not a newline", end="")
-------------------------------------------------------
          print ("Hello")
          print ("Hello", "world")
-------------------------------------------------------
          #!/usr/bin/python

          import sys

          teeth = "white"
          coal = "black"

          print teeth,"teeth and",coal,"shoes"
          print teeth," - teeth and - ",coal," - shoes"

          teeth = "yellow"; coal = "red"
          print teeth,"teeth and",
          print coal,"shoes"

          print >> sys.stderr, "Error and logging message"


##In 3.0

          basket = ('Apple', 'Oranges', 'Banana')
          print (*basket, sep=", ", end=".\n")
-------------------------------------------------------
          print ("Hello")
          ("Hello", "world")
-------------------------------------------------------
          #!/usr/local/bin/python3.0

          import sys

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

          print ("Error and logging message",file = sys.stderr)
