# Dunder Methods

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:

```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"

```
To fix this, you can add a __len__ dunder method to your class:

```
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```

## Object Initialization: __init__

To construct account objects from the Account class I need a constructor which in Python is the ```__init__``` dunder



## Object Representation: __str__, __repr__

```__repr__:``` The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.


```__str__:``` The “informal” or nicely printable string representation of an object. This is for the enduser.

# Iteration: __len__, __getitem__, __reversed__


In order to iterate over our account object I need to add some transactions. So first, I’ll define a simple method to add transactions. I’ll keep it simple because this is just setup code to explain dunder methods, and not a production-ready accounting system:
```
def add_transaction(self, amount):
    if not isinstance(amount, int):
        raise ValueError('please use int for amount')
    self._transactions.append(amount)

 ```

# conclusion of dunder methods
- Initialization of new objects. ```__init__```

- Object representation. ```__str__, __repr__```

- Enable iteration. ```__len__, __getitem__, __reversed__```

- Operator overloading (comparison). ```__eq__, __lt__```

- Operator overloading (addition) ```__add__```

- Method invocation. ```__call__```

- Context manager support (with statement). ```__enter__, __exit__```


# Probability in Python:

What is probability?
At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur. The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:

Flipping a heads.
Flipping a tails.


## The data and the distribution
Intuitively, we’d like to use the scores of the wines to compare groups, but there comes a problem: the scores usually fall in a range. How do we compare groups of scores between types of wines and know with some degree of certainty that one is better than the other? Enter the normal distribution. The normal distribution refers to a particularly important phenomenon in the realm of probability and statistics.

In a probability context, the high point in a normal distribution represents the event with the highest probability of occurring. As you get farther away from this event on either side, the probability drops rapidly, forming that familiar bell-shape. The high point in a statistical context actually represents the mean. As in probability, as you get farther from the mean, you rapidly drop off in frequency. That is to say, extremely high and low deviations from the mean are present but exceedingly rare.