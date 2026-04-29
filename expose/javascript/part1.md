# Part 1 (Variables & Scope)

## Question 1

'values added: 20' is printed by line 9. 'result' is declared/initialized in the same ('if') block as it is used (displaying to console).

## Question 2

'final result: 20' is printed at line 13 because 'var' has no block scope, and rather has function-scope so 'var' can be accessed anywhere in the function it is declared in. If 'var' is declared outside of any functions, then it is a global variable and can be used anywhere. 'var' retains its value of 20 from inside the 'if' block.

## Question 3

You should not use 'var' because it is function-scoped instead of block-scoped, so a variable declared with 'var' inside an 'if' block or 'for' loop can still be accessed outside of it, which can cause unexpected bugs and naming conflicts. 'var' is global-scoped when declared outside of any function, so it can be messy when accessing or naming future variables. 'let' and 'const' are block-scoped and thus are easier to work with and debug.

## Question 4

'values added: 20' is printed at line 9 because 'let' has block scope, and since line 9 is still inside of the 'if' block where 'result' is declared with 'let', line 9 can still access 'result'.

## Question 5

An error occurs at line 13: 'ReferenceError: result is not defined'. This is because 'let' is block-scoped, so 'result' only exists inside the 'if' block it was declared in, and at line 13 we are outside of that block, so 'result' is no longer in scope.

## Question 6

An error occurs before line 9 is reached: 'TypeError: Assignment to constant variable'. This is because 'const' declares a variable that _cannot_ be reassigned after it is declared or initialized. Line 7 tries to reassign 'result' from 0 to 'num1 + num2', so the error is thrown and line 9 is never reached.

## Question 7

Line 13 is also never reached because line 7 throws the 'TypeError: Assignment to constant variable'.
