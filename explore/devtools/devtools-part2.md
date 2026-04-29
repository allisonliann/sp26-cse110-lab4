# DevTools Debugging

## Q1

The bug what that num1 and num2 were treated as strings, so the + operator on strings concatenated them instead of adding them as numbers, so 2 and 3 gave "23" instead of 5.

## Q2

I would fix by converting num1 and num2 to numbers using Number() before adding them (type conversion or type cast) so the + operation performs arithmetic addition instead of string concatenation.
