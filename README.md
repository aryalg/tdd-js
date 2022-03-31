
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

Many of you might object, "But what's the point of that? Isn't that just a lot of pointless extra bother?"

It’s true that setting up the testing environment and figuring out how to unit write tests often takes some effort. In the short run, it's faster to just do things the traditional way. But in the long run, TDD can save time that would otherwise be wasted manually testing the same thing repeatedly. And it just so happens that there are a number of other benefits to unit testing:

## Benefits of TDD

### Automatic regression detection
Sometimes you'll write a bug in your program that causes code that used to function properly to no longer do so, or you'll accidentally reintroduce an old bug that you previously fixed. This is called a regression. Regressions might sneak by unnoticed for a long time if you don't have any automated testing. Passing your unit tests doesn’t guarantee that your code works correctly, but if you write tests for every bug you fix, one thing passing your unit tests can guarantee is that you haven't reintroduced an old bug.
### Bold refactoring
Code can get messy pretty quickly, but it's often scary to refactor it since there's a good chance that you'll break something in the process. After all, code often looks messy because you had to hack together some workarounds to make it work for rare edge cases. When you try to clean it up, or even rewrite it from scratch, it's likely that it will fail on those edge cases. If you have unit tests covering these edge cases, you'll find out immediately when you've broken something and you can make changes more courageously.
### Documentation
If another developer (or perhaps the future you) can't figure out how to use the code you've written, they can look at the unit tests to see how the code was designed to be used. Unit tests aren't a replacement for real documentation, of course, but they're certainly better than no documentation at all (which is all too common, since programmers almost always have things higher on their priority lists than writing documentation).
### Robustness
When you have no automated testing and applications become sufficiently complex, it’s easy for the code to feel very fragile. That is, it seems to work fine (most of the time) when you use it, but you have a nagging anxiety that the slightest unexpected action from the user or the slightest future modification to the code will cause everything to crash and burn. Knowing that your code passes a suite of unit tests is more reassuring than knowing that your code seemed to work when you manually tested it with a handful of examples the other day.





