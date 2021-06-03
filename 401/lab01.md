# pain and suffering

All growth comes with some degree of pain, as it pulls you out of your comfort zone. The greater the growth, the greater the pain. But pain in the service of growth is a good thing, as long as that pain is what’s necessary to achieve the growth that you’re aiming for. And even better than that, this pain is only temporary. It’s what will launch you forward into the next phase of your life.

Do not confuse this with suffering.

Suffering is pain without purpose. Pain with no higher goal. Pain with no dreams, no ambition, no aspiration.



# Big O Notation
Big O notation is:

- used in Computer Science to describe the performance or complexity of an algorithm.

- describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.


# Common Orders Of Growth

1- O(1)

- describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

- Example:

bool IsFirstElementNull(IList elements) {return elements[0] == null;}

2- O(N)

- An algorithm with linear behaviour and is directly proprtional with the input data set size.

- Example(showing how this order favours the worst-case performance scenario): 

bool ContainsValue(IEnumerable string> elements, string value) { foreach (var element in elements) { if (element == value) return true; }
return false; }

3- O(N²)

- An algorithm that is directly proprtional with the square of the input data set size.
common among algorithms with nested iterations over the data set.

- Example:
bool ContainsDuplicates(IList elements) { for (var outer = 0; outer < elements.Count; outer++) { for (var inner = 0; inner < elements.Count; inner++) { // Don't compare with self if (outer == inner) continue;

```
      if (elements[outer] == elements[inner]) return true; 
  }


```

4- O(2^N)

- an algorithm whose growth doubles with each addition to the input data set.

The growth curve of an O(2^N) function is exponential — starting off very shallow, then rising meteorically.

- Example:

recursive calculation of Fibonacci numbers