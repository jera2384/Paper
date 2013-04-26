Outline
=======

* __Introduction__: discuss the language Python, the overall concept of print, and why a change in how to use print is noteworthy due to the universal need of it.
* __Print as a Statement__
  * Syntax of a statement - simplicity, ease of flow and writing is nice and a pro in the community's eyes.
  * Difficulties include only being able to print out certain information, can only use print statements at a certain place in code, etc.
  * Originally made a statement in order to be as simple as possible (expand)
* __Reasons to Change__
  * Quote official PEP 3105:
      * "If print() is a function, it would be much easier to replace it within one module (just def print(*args):...) or even throughout a program." This would allow for much more widespread use throughout the code, easier to evolve the function.
      * "print is the only application-level functionality that has a statement dedicated to it. Within Python's world, syntax is generally used as a last resort, when something can't be done without help from the compiler. Print doesn't qualify for such an exception." Keeps more true to the nature of the Python language.
  * Turning print into a function, overall, allows print to be significantly more flexible. It is able to evolve and add on new helper functions, convert items, etc. that members of the community might find useful. Without this change, print is simpler, but capable of significantly fewer things. Plus, this print as a function can still be used as a statement, so it is backwardly compatible.
* __Print as a Function__
  * Syntax of a function - has parameters (see specifications resource)
  * Flexibility of the function - where and how it can be used, what can be used with it, etc.
* __Overall Community Response__
  * Generally positive. Print being a statement is quoted as one of python's great regrets, so it fits in much better as a function.
  * People like the power-- it is what they expect a print to be able to do, especially with the influence/similarity to the power in other language's prints, like printf()
  * Since programmers are still fully able to write as they did when print was a statement, the change can be made slowly over time if people do not have a need for the higher functionality.
* __Overall Analysis__
  * Making the change from print as a statement to a function needed to be done at some point, from the feel of the community and language makers as a whole.
  * Overall functionality is greatly improved, and still easy to transition for people with less code intuition since it is backwards compatible.
