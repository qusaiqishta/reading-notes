# What Are Dunder Methods?
In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them. You should treat these methods like a normal language feature.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:
```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
To fix this, you can add a __len__ dunder method to your class:

class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```

## Enriching a Simple Account Class
- Initialization of new objects
- Object representation
- Enable iteration
- Operator overloading (comparison)
- Operator overloading (addition)
- Method invocation
- Context manager support (with statement)

### Object Initialization: __init__
Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:
```
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []
 ```
The constructor takes care of setting up the object. In this case it receives the owner name, an optional start amount and defines an internal transactions list to keep track of deposits and withdrawals.

This allows us to create new accounts like this:
```
>>> acc = Account('bob')  # default amount = 0
>>> acc = Account('bob', 10)
```

### Object Representation: __str__, __repr__
It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1- __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

2- __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

### Iteration: __len__, __getitem__, __reversed__
In order to iterate over our account object I need to add some transactions. So first, I’ll define a simple method to add transactions

```
class Account:
    # ... (see above)

    def __len__(self):
        return len(self._transactions)

    def __getitem__(self, position):
        return self._transactions[position]
```

### Operator Overloading for Comparing Accounts: __eq__, __lt__
We all write dozens of statements daily to compare Python objects:
```
>>> 2 > 1
True

>>> 'a' > 'b'
False
```
This feels completely natural, but it’s actually quite amazing what happens behind the scenes here. Why does > work equally well on integers, strings and other objects (as long as they are the same type)? This polymorphic behavior is possible because these objects implement one or more comparison dunder methods.

An easy way to verify this is to use the dir() builtin:
```
>>> dir('a')
['__add__',
...
'__eq__',    <---------------
'__format__',
'__ge__',    <---------------
'__getattribute__',
'__getitem__',
'__getnewargs__',
'__gt__',    <---------------
...]
```

```
from functools import total_ordering

@total_ordering
class Account:
    # ... (see above)

    def __eq__(self, other):
        return self.balance == other.balance

    def __lt__(self, other):
        return self.balance < other.balance
And now I can compare Account instances no problem:

>>> acc2 > acc
True

>>> acc2 < acc
False

>>> acc == acc2
False
```

### Operator Overloading for Merging Accounts: __add__

```

def __add__(self, other):
    owner = '{}&{}'.format(self.owner, other.owner)
    start_amount = self.amount + other.amount
    acc = Account(owner, start_amount)
    for t in list(self) + list(other):
        acc.add_transaction(t)
    return acc
```

### Callable Python Objects: __call__
You can make an object callable like a regular function by adding the __call__ dunder method. For our account class we could print a nice report of all the transactions that make up its balance:
```
class Account:
    # ... (see above)

    def __call__(self):
        print('Start amount: {}'.format(self.amount))
        print('Transactions: ')
        for transaction in self:
            print(transaction)
        print('\nBalance: {}'.format(self.balance))
```        
Now when I call the object with the double-parentheses acc() syntax, I get a nice account statement with an overview of all transactions and the current balance:
```
>>> acc = Account('bob', 10)
>>> acc.add_transaction(20)
>>> acc.add_transaction(-10)
>>> acc.add_transaction(50)
>>> acc.add_transaction(-20)
>>> acc.add_transaction(30)

>>> acc()
Start amount: 10
Transactions:
20
-10
50
-20
30
Balance: 80
```

### Context Manager Support and the With Statement: __enter__, __exit__
A context manager is a simple “protocol” (or interface) that your object needs to follow so it can be used with the with statement. Basically all you need to do is add __enter__ and __exit__ methods to an object if you want it to function as a context manager.



## Python Iterators 
Iterators provide a sequence interface to Python objects that’s memory efficient and considered Pythonic. Behold the beauty of the for-in loop!
To support iteration an object needs to implement the iterator protocol by providing the __iter__ and __next__ dunder methods.
Class-based iterators are only one way to write iterable objects in Python. Also consider generators and generator expressions.

## Python Generators – A Quick Summary
Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.
The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.
Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.