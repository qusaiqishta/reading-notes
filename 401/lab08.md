# List Comprehensions in Python

List comprehensions provide a concise way to create lists.

It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses. The expressions can be anything, meaning you can
put in all kinds of objects in lists. The list comprehension always returns a result list.


For example:

```
new_list = []
for i in old_list:
    if filter(i):
        new_list.append(expressions(i))

```

can be written :


```
new_list = [expression(i) for i in old_list if filter(i)]

```


## General syntex for list comprehension:

```
[ expression for item in list if conditional ]

```

**Note that: you can add a function instead of expression**

this is equivalent to

```
for item in list:
    if conditional:
        expression

```

a simple examples:


```
# You can either use loops:
squares = []

for x in range(10):
    squares.append(x**2)
 
print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Or you can use list comprehensions to get the same result:
squares = [x**2 for x in range(10)]

print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

```


```

string = "Hello 12345 World"
numbers = [x for x in string if x.isdigit()]
print numbers

>> ['1', '2', '3', '4', '5']

```

## First-Class Objects

 functions are first-class objects. This means that functions can be passed around and used as arguments

 ```
def greet_bob(greeter_func):
    return greeter_func("Bob")
 ```

 ## Inner Functions
It’s possible to define functions inside other functions. Such functions are called inner functions.

Furthermore, the inner functions are not defined until the parent function is called. They are locally scoped to parent(): they only exist inside the parent() function as local variables. Try calling first_child(). You should get an error . Whenever you call parent(), the inner functions first_child() and second_child() are also called


# Simple Decorators

```
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

def say_whee():
    print("Whee!")

say_whee = my_decorator(say_whee)  # The so-called decoration happens at this line

```
Can you guess what happens when you call say_whee()? Try it:

```
>>> say_whee()
Something is happening before the function is called.
Whee!
Something is happening after the function is called.
```


## Syntactic Sugar!
The way you decorated say_whee() above is a little clunky. First of all, you end up typing the name say_whee three times. In addition, the decoration gets a bit hidden away below the definition of the function.

Instead, Python allows you to use decorators in a simpler way with the @ symbol, sometimes called the “pie” syntax. The following example does the exact same thing as the first decorator example:
```
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_whee():
    print("Whee!")

```    