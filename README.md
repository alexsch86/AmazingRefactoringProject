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

Examples of first rules that are violated:

 ### Express intent
 
Rename doit method to better express what is doing: addLinesToBuffer.

 ###  