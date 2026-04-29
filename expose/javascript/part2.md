# Part 2 (A Little More of a Challenge)

## Question 1

'3' is printed at line 12 because 'var i' has function scope so it is accessible outside of the 'for' loop. The length of prices is 3, and the 'for' loop ends when i gets to 3 and the condition is not satisfied, so i is 3 at the end of the 'for' loop.

## Question 2

'150' is printed at line 13 because 'var discountedPrice' has function scope so it can be accessed outisde of the 'for' loop. The last (most recent) value of 'discountedPrice' was 'prices[2] _ (1 - 0.5) = 300 _ 0.5 = 150'.

## Question 3

'150' is printed at line 14 because 'var finalPrice' is function-scoped and declared outside the 'for' loop, so it can still be accessed at line 14. The last value after the loop was 'Math.round(150 \* 100) / 100 = 150'.

## Question 4

The function returns '[50, 100, 150]' because 'discounted' is an array and the loop fills the array with each discounted price as we iterate over the 'prices' array. The 'console.log' lines are all commented out so nothing is printed.

## Question 5

An error: 'ReferenceError: i is not defined' is thrown at line 12 because 'let i' is block-scoped to the 'for' loop so outside at line 12, 'i' no longer exists in scope.

## Question 6

An error: 'ReferenceError: discountedPrice is not defined' is thrown at line 13 because 'let discountedPrice' is block-scoped to the 'for' loop so outside at line 13, 'discountedPrice' no longer exists in scope.

## Question 7

'150' is printed at line 14 because 'let finalPrice = 0' is declared/initialized at the function scope, outside of the 'for' loop, so it can be accessed at line 14 which is still inside the function and also outside the 'for' loop. The last value after the loop was 'Math.round(150 \* 100) / 100 = 150'.

## Question 8

The function returns '[50, 100, 150]' because 'let discountedPrice' is block-scoped inside the 'for' loop, and 'let finalPrice' is function-scoped.

## Question 9

An error: 'ReferenceError: i is not defined' is thrown at line 11 because 'let i' in the 'for' loop is block-scoped to the loop so outside at line 11, 'i' is not defined.

## Question 10

'3' is printed at line 12 because 'const length = prices.length' is declared at the function scope outside the 'for' loop so it can be accessed at line 12. Length of prices is 3 so 'i' ends at 3 (when the condition fails and we break out of the 'for' loop).

## Question 11

The function returns '[50, 100, 150]' because 'const discountedPrice' is block-scoped inside the loop (a new const is created each iteration, which is allowed); the discounted prices are filled in to 'discounted' and returned.

## Question 12

A. student.name
B. student['Grad Year']
C. student.greeting()
D. student['Favorite Teacher'].name
E. student.courseLoad[0]

## Question 13

A. '32' because the number 2 is converted to string '2' and the + operator with a string does concatenation, so '3' + '2' = '32'.
B. 1 because the string '3' is converted to number 3 and the - operator always does arithmetic subtraction so 3 -2 = 1.
C. 3 because null converts to 0 in numeric circumstances.
D. '3null' because null converts to the string 'null' and the + operator with a string does concatenation.
E. 4 because true converts to 1 in numeric context.
F. 0 because false and null convert to 0 in numeric circumstances.
G. '3undefined' because undefined converts to the string 'undefined' and the + operator with string is concatenation.
H. NaN because the - operator tries numeric conversion so '3' converts to 3 but undefined converts to NaN and any arithmetic with NaN returns NaN.

## Question 14

A. true because the string '2' is converted to number 2 for comparison and 2>1.
B. false because both are strings so lexicographic comparison: '2' has larger ASCII code than '1' so '2' < '12' is false.
C. true because == operator performs type coercion so string '2' is converted to number 2.
D. false because === operator does _NOT_ perform type coercion; 2 is a number while '2' is a string so different types.
E. false because true converts to number 1.
F. true because Boolean(2) converts 2 to a boolean and any non-zero numbers converts to true.

## Question 15

The == operator (loose equality) performs type coercion before comparing, so it converts both values to the same type if they differ before checking equality. However, === operator (strict equality) does NOT perform type coercion so the value AND type must match to return true. === is preferred because avoids bugs caused by automatic type conversion.

## Question 17

The result is [2, 4, 6] because:

- modifyArray creates an empty array newArr
- Loops through [1, 2, 3]
- For each element, it calls callback(array[i] which is doSomething(array[i]))
- doSomething multiplies each number by 2
- Each result is pushed into newArr, which is then returned

## Question 19

Output is:
1
4
3
2

This is because console.log(1) runs immediately and prints 1. Then setTimeout(..., 1000) schedules log(2) to run after 1000ms. setTimeout(..., 0) schedules log(3) to run after 0ms, but it still goes into the queue and waits for synchronous code to finish first. console.log(4) runs immediately and prints 4. After all synchronous code finishes, queue runs so log(3) runs first with no delay and prints 3, then log(2) runs after 1 second and prints 2.
