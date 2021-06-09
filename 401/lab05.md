# Linked list

Is a data structure that contains nodes that links/points to the next node in the list and has two types

- Singly : Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

- Doubly : Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

## So what is a node??

Node or Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

### Node has some properties

- Next - Each node contains a property called Next. This property contains the reference to the next node.

- Head - The Head is a reference of type Node to the first node in a linked list.

- Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.

The picture bellow explain the singly list

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList1.PNG)


## Traversal

When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing

### How to approach the traversal ??

The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.

When traversing through a linked list, the Current variable will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.


###  Traversal Example
Let’s put a use case on our traversal. We want to check whether or not our LinkedList Includes a specific value.

```
ALGORITHM Includes (value)
// INPUT <-- integer value
// OUTPUT <-- boolean

  Current <-- Head

  WHILE Current is not NULL
    IF Current.Value is equal to value
      return TRUE

    Current <-- Current.Next

  return FALSE

```

## Adding a node 
1-At the beginning of the list

An example can be with adding a node to a linked list by using Add() method. If we want to add a node with an O(1) efficiency, we have to replace the current Head of the linked list with the new node, without losing the reference to the next node in the list.


![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList2.PNG)


```
ALGORITHM Add(newValue)
// INPUT <-- Value to add
// OUTPUT <-- No output

  newNode <-- NEW Node
  newNode.Value <-- newValue
  newNode.Next <-- Head
  Head <-- newNode
```

2- Not in the beginning 

=> this happen by using AddAfter or AddBefor methods

example : nsert node6 before node4.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LLInsert3.PNG)


 - Current is pointing to node3.
- node3.Next property is equal to node4.
- Since this is the node we want to insert before, we can now set our node6.Next property also to node4. We do this at the time the node is found to prevent setting node6.Next to a node that may not exist.

- Uh-Oh, now both node3 and node6 are pointing to the same next node. node6 is not quite fully apart of the linked list.

- Next, we have to adjust node3.Next to point to the newly created node, node6. Since we still have Current pointing to node3 this will be a straightforward transaction. We just simply tell Current (because it is pointing to the same memory location as node3) to change it’s Next to point to the new node (node6).

```
ALGORITHM AddBefore(newValue, valueToAddBefore)
// INPUT <-- New value, Value to add before
// OUTPUT <-- boolean

  Current <-- Head

  IF Current is equal to NULL
    return FALSE

  WHILE Current.Next is not equal to NULL
    IF Current.Next.Value is equal to valueToAddBefore
      newNode <-- NEW Node
      newNode.Value <-- newValue
      newNode.Next <-- Current.Next
      Current.Next <-- newNode
      return TRUE

    Current <-- Current.Next;

  return FALSE

```