# What is a stack

A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

Common terminology for a stack is

- Push - Nodes or items that are put into the stack are pushed
- Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
- Top - This is the top of the stack.
- Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
- IsEmpty - returns true when stack is empty otherwise returns false.


# Stack Visualization

Here’s an example of what a stack looks like. As you can see, the topmost item is denoted as the top. When you push something to the stack, it becomes the new top. When you pop something from the stack, you pop the current top and set the next top as top.next.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)



# What is a Queue

Common terminology for a queue is

- Enqueue - Nodes or items that are added to the queue.
- Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
- Front - This is the front/first Node of the queue.
- Rear - This is the rear/last Node of the queue.
- Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
- IsEmpty - returns true when queue is empty otherwise returns false.


![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)



# conclusion

Stacks and queues have a lot of things in common.
They are both linear data structures in that you have one element and another
element and then another element. They are both flexible with their sizes so
you don't have to allocate initially them to have a size like 50, you can just
add elements as you go and then also shrink it down. The main difference comes
in how elements are removed from the stack or from the queue. A stack is what
would be called a LIFO data structure, last in first out.
It's much like an actual stack of plates. The last plate you put on top of that
stack, that's going to be the first one you remove, its LIFO, last in first out.
A queue though, is FIFO, first in first out. So think about a queue or line of people
waiting to get into a movie theater. When the movie theater doors open
they don't first serve the person who just hopped into line five seconds ago.
They serve the person who got in line at the very very beginning an hour or two ago, and
then the next person and then the next person. The very first person in is the very first
person removed.

That's what FIFO means, first in first out. 