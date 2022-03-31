
# What is Test Driven Development?
Test Driven Development (TDD) is software development approach in which test cases are developed to specify and validate what the code will do. TDD starts with developing tests for every small functionality. Simple concept of TDD is to write and correct the failed tests before writing new code.

##### Traditionally, software development flow follows this setps:
- Think about what your code suppose to do?
- Write do to achieve that functionality
- Test the Code to see if it works

#### Example
Suppose, we have a funtion which add two number `add(number1, number2)`. While following traditional approach first we write function `add` now we'll need to test it by passing multiple numbers. We could write `add(1,1)`, `add(5,7)` and `add(-4, 5)`. Result of the function can have 2, 12, and opps -9. There should be bug somewhere which is giving result of -9 instead of 1.

After going through the bug, we revise it to fix the associated issue and we run function `add(-4, 5)` again. May be this will return 1, just like we wanted. But what if other case break where `add(5,7` which return -2. We'll go through few cycle to fix everything by revising the code until we're sufficiently confident that our code works just the way we want.

##### TDD Software development flow
- Think about what your code is supposed to do.
- Write tests specifying what you expect your code to do.
- Write the code to do it.
- See if the code works by running it against the tests you wrote

```js
expect(add(1,1)).toEqual(2);
expect(add(5,7)).toEqual(12);
expect(add(-4,5)).toEqual(1);
```





