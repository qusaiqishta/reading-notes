# Unit tests and TDD
Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.

But Test-Driven Development is a strategy to think (and write!) tests first.

The test file name should follow the same name of module name. For instance, if our module is gender.py, our test name should be test_gender.py. It’s ideal to separate the tests folder from production code (the implementation)

Other thing to care about is the structure. A convention widely used is the 

AAA: Arrange, Act and Assert.

- Arrange: you need to organize the data needed to execute that piece of code (input);

- Act: here you will execute the code being tested (exercise the behaviour);

- Assert: after executing the code, you will check if the result (output) is the same as you were expecting.


## The Cycle
- rite a unit test and make it fail 

- Write the feature and make the test pass!

- Refactor the code


# Recursion

The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily

Example of Recrusion 

finding the sum of numbers between 1 and n

```
approach(1) – Simply adding one by one

f(n) = 1 + 2 + 3 +……..+ n

```



```
approach(2) – Recursive adding 

f(n) = 1                  n=1

f(n) = n + f(n-1)    n>1

```

There is a simple difference between the approach (1) and approach(2) and that is in approach(2) the function “ f( ) ” itself is being called inside the function, so this phenomenon is named as recursion and the function containing recursion is called recursive function, at the end this is a great tool in the hand of the programmers to code some problems in a lot easier and efficient way.


## What is the difference between direct and indirect recursion? 


A function fun is called direct recursive if it calls the same function fun. A function fun is called indirect recursive if it calls another function say fun_new 