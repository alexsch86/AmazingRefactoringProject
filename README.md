# Increase productivity with a refactoring exercice

A gradle-based project for refactoring. Original project is at: 
 - https://github.com/f-lombardo/AmazingRefactoring
 
 
 ## Methodology of work
 
 Let's refactor this application taking in account the [4 rules of simple design](https://www.theguild.nl/4-rules-of-simple-design/).
 
 These 4 rules are:
 
 * Tests passes
 * Express intent
 * No duplication
 * Small 
 
 ## Tips for refactoring 
 
Try at each step to see what rule out of the 4 is violated and can be dealt with, without breaking a more important rule above.
To have a better view of how to rename methods and their variables, for expressiveness, use the debugger step by step.

Examples of rules that are violated:

 ### Express intent
 
Rename doit method to better express what it does: addAllMazeLinesToBuffer.
Do the same for the clear, println, print, rnd and GOTO methods.

 ### Duplication

 Inline variables h and v from the initial doit method to use actual method parameters, which are also more expressive.

 ### Express intent

 The horizontal and vertical method parameters should tell better their intent -> generatingMatrixLines and generatingMatrixColumns.

 ### Express intent

 Rename variables of initial doit method q, z, x, c, r, s.

 ### Small

Extract the common logic from the big switch loop. To do that, you can see what target values have only 2 occurrences. For each such target
value, inline the case of this target value in the GOTO (initial method name) call with this number. Repeat doing so, to reduce the case
statements and to have a clearer view of the flow of the code in the switch. Eventually, you can either extract methods for common if else
code and delete unused code, if there are such cases.


 ** One more tip

You can create additional tests, by playing with the seed and generating matrix number of lines and columns. In each test, take the output
text generated and keep it for the test to pass. See the output mazes and go through the debug steps to see the patterns of maze generation.