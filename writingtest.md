## Unit Tests:
1. A function called `multiplication` that returns the product of the two input numbers.

## Expectations:
* the function will return a number which is the product of numbers
* the function takes one argument
* the argument is an array of two numbers
* we would expect `multiply[2 * 5]` to return 10
* the function will return an error if there are any empty 

## Test Specs:
1. Expect `mupltiplication([2 * 5])` to be equal to 10
2. Expect `mupltiplication([10 * 10])` to be equal to 100
3. Expect `mupltiplication([])` to be equal to 0
4. Expect `mupltiplication([9 * 6])` to be equal to 54
5. Expect `mupltiplication()` to be an error

2. A function called "concatOdds" takes two arrays of integers as arguments. It should return a single array that only contains the odd numbers, in ascending order, from both of the arrays.
    * Example: concatOdds([3, 2, 1], [9, 1, 1, 1, 4, 15, -1])
        * ...should result in [-1, 1, 3, 9, 15]
    * Think about the following; you may need to make assumptions or decisions about the prompt and how the code should behave:
        * What should happen with unexpected inputs?
            * What kinds of unexpected inputs should we worry about?
        * What should happen when there are multiples of the same odd number in the arrays? (Hint: We gave you the answer to this one in the example above.)

## Expectations:
* the function takes two arrays of integers as arguments
* the function will return a single array that only contains the odd numbers
* the functions returned array will contain numbers in ascending order from both arrays put in 
* the argument is two arrays that contain odd integers
* we expect `concatOdds([1, 4, -3], [13, 15, 2])` to return [-3, 1, 13, 15]

## Test Specs
1. Expect `concatOdds([1, 4, -3], [13, 15, 2])` to result in `[-3, 1, 13, 15]`
2. Expect `concatOdds([2, 2, 8, 14], [13])` to result in `[13]`
3. Expect `concatOdds([])` to result in `[]`
4. Expect `concatOdds(["be one"])` to result in an error
5. Expect `concatOdds([], [-5, 11]` to result in `[-5, 11]`
6. Expect `concatOdds([1, 2, 3, 3, 2, 1, 3], [1])` to result in `[1, 3]`

## Functional Tests:
1. A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.
    * Think about the following; you may need to make assumptions or decisions about the prompt and how the feature should behave:
        * What should happen if the cart is empty?
        * What needs to be shown to the user at each step of check out?
        * What behaviors of this feature does the prompt miss or gloss over?
    * Hint: Observe the shopping cart and checkout features of some popular websites to get some ideas!