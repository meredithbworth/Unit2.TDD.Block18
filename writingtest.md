## Unit Tests:
1. A function called `multiplication` that returns the product of the two input numbers.

## Expectations:
* the function will return a number which is the product of numbers
* the function takes one argument
* the argument is an array of two numbers
* we would expect `multiply[2, 5]` to return 10
* return `undefined` or `0` for any errors

## Test Specs:
1. Expect `mupltiplication([2, 5])` to be equal to 10
2. Expect `mupltiplication([10, 10])` to be equal to 100
3. Expect `mupltiplication([5])` to return `undefined` or `0`
4. Expect `mupltiplication([9, 6])` to be equal to 54
5. Expect `mupltiplication()` to return `undefined` or `0`
6. Expect `mupltiplication(["2", 1])` to return `undefined` or `0`

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
* for all errors, result in `undefined` or `0`
* any passed in, empty arrays will return an empty array `[]`
* we expect `concatOdds([1, 4, -3], [13, 15, 2])` to return [-3, 1, 13, 15]

## Test Specs
1. Expect `concatOdds([1, 4, -3], [13, 15, 2])` to result in `[-3, 1, 13, 15]`
2. Expect `concatOdds([2, 2, 8, 14], [13])` to result in `[13]`
3. Expect `concatOdds([])` to result in `undefined` or `0`
4. Expect `concatOdds(["be one"])` to result in `undefined` or `0`
5. Expect `concatOdds([], [-5, 11]` to result in `[-5, 11]`
6. Expect `concatOdds([1, 2, 3, 3, 2, 1, 3], [1])` to result in `[1, 3]`
7. Expect `concatOdds([10, 10, 11], [1, 3, 4], [10, 10, 5])` to result in `[1, 3, 5, 11]`

## Functional Tests:
1. A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.
    * Think about the following; you may need to make assumptions or decisions about the prompt and how the feature should behave:
        * What should happen if the cart is empty?
        * What needs to be shown to the user at each step of check out?
        * What behaviors of this feature does the prompt miss or gloss over?
    * Hint: Observe the shopping cart and checkout features of some popular websites to get some ideas!

## Expectations:
* user intends to check out items in their cart as a logged-in user, so is prompted to put in login and password then submit form
* if user doesn't have an account, they can either continue "as guest" or "create account" for the first time
* if user has forgotten that they've created an account in the past and put in the same credintials for an already used log in (username or email address), it will alert them in red font that 'that login information is already in use'
* a valid/new login will be confirmed with a green check mark
* this form only accepts email address that are confirmed with '@' symbol
* password must meet the following requirements
    - at least 7 characters
    - cannot contain any special characters
    - must contain at least one number and one capitalized letter
    - cannot have any repeated characters i.e. rhe1uu90
* must retype the exact same password to continue
* a vaild password will be confirmed with a green check mark
* if the cart is empty, it will display a 'return to shopping' button and state 'your cart is empty' with no prompts for logging in
* when officially checking out as either a guest or member, it asks to confirm shipping method
* prompted to complete a form for shipping details which includes:
    - first name
    - last name
    - address
    - city
    - etc.
* continue to payment button will become accessible once this is filled
* any address errors will light up in red before allowed to continue to payment methods
* select PayPal, credit card, or payment plan and going to third party payment page if prompted (PayPal or other)
* Review Order button becomes accessible
* Make any final edits to your order details
* Click submit order, which will return a Successfully Submitted Order page with the order number
* receive a confirmation email within 30 minutes of clicking the submit order and receiveing the 'success' page


## Test Specs
GIVEN I just opened the site as a new user
WHEN I navigated to my cart which is empty
THEN I am prompted to return to shopping (so that I might add items to the cart)

GIVEN I would like to purchase a jacket
WHEN I search for jackets and find one that might fit me
THEN I select the correct color, size, and add it to my cart

GIVEN I am a new user (as far as I remember)
WHEN I go to my cart and select the 'checkout' button
THEN I am prompted to login or continue to checkout as a guest

GIVEN I have selected to continue as a guest
WHEN I click the 'continue as guest button'
THEN I am asked to select my shipping method

GIVEN that I have selected the shipping method
WHEN I scroll to choose payment options
THEN I am halted and the shipping address section is highlighted in red text

GIVEN I have added my shipping information
WHEN I then click 'choose payment options'
THEN the page changes to list a drop down for payment options

GIVEN I want to pay with my credit card
WHEN I select from the payment option dropdown menu 'credit card'
THEN I am asked which type of card do I plan to use

GIVEN that I put in Visa as my card
WHEN I put in the digits of my card number, but mistakenly but in 15 digits
THEN It alerts to me in red text that I have not entered a valid card number

GIVEN that I have corrected the number error
WHEN I add in my billing information
THEN the button to review the order becomes accessible and is highlighted

GIVEN that my order is correct along with shipping and payment details
WHEN I click 'Submit'
THEN I see a new page stating "You have successfully submitted your order and will receive a confirmation email shortly"