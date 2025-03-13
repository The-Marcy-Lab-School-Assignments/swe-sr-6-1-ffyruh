# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Arrays, Linked Lists and Doubly Linked Lists all allow programmers to organize data in a sequence. So, how would you choose to use one over the other?

In your response, make sure to compare the time complexities for insertion, removal, and random access (grabbing a particular known element by index/position) for each data structure as well as memory usage and ease of traversal.

### Response 1

Looking at these data structures' time complexity makes their specific applications intuitive.

Array Complexities:
- Time
  - Prepend to start - `O(n)`
  - Append to end - `O(1)`
  - Insertion/Deletion - `O(n)`
  - Search - `O(log n)` to `O(n)`
  - Random Access - `O(1)`
- Space - `O(n)`

An array is particularly good at random access, appending to the end (hint: using it as a stack!), and search. Compared the other structures, arrays **may** also have the advantage of being the most lightweight in terms of space.

Linked List Complexities:
- Time
  - Prepend to start - `O(1)`
  - Append to end - `O(1)` to `O(n)`
  - Insertion/Deletion - `O(n)`
  - Search - `O(n)`
  - Random Access - `O(n)`
- Space - `O(n)`

Linked lists are beneficial when you are accessing the start and the end frequently at the same time. In both cases, it is as fast as `O(1)`, since you don't have to shift every item when prepending (unlike an array). In terms of search and random access, linked lists in general would be a terrible choice. Traversal has to be done manually from preexisting pointers (which is typically only the head and the tail). If you see yourself wanting to have access to more than those two nodes frequently, it might the perfect time to defer to an array (or even an object).

Doubly Linked Lists:
- Time
  - Prepend to start - `O(1)`
  - Append to end - `O(1)` to `O(n)`
  - Insertion/Deletion - `O(n)`
  - Search - `O(n)`
  - Random Access - `O(n)`
- Space - `O(n)`

Doubly linked lists are no different than linked lists in terms of time complexity, though it has the added benefit of simplifying some methods like insertion/deletion. One specific advantage is if the linked list is sorted, and that you would want to iterate over it in reverse. All nodes having a bidirectional pointer makes this possible.

## Prompt 2

Imagine you are developing a web browser's "back" button functionality. When a user clicks "back," the browser should navigate to the previously visited webpage.

Would you use a stack or a queue to implement this functionality?

In your response, explain what a Stack/Queue is and why it would be best for this use case. Make sure that your response includes the terms LIFO or FIFO.

### Response 2

Any kind of redo/undo mechanism calls for a stack. This is because the concept of going back and forth means referencing the most recent, immediate action performed in both ways. You will typically not directly interact with the actions done way back in history. A stack is designed for this purpose, where you only have a reference to the topmost element which you can choose to access/pop/replace (with a push). You can technically stick with a queue and ignore the fact that you have a pointer to the leftmost (earliest) element and perform the same operations you could do with stacks but... that needs no explanation.

## Prompt 3

What is an Abstract Data Type and why are they worth learning about?

### Response 3

An abstract data type is just a way we can describe behaviors we want without setting into concrete how we want it to be implemented or how we want the data to be organized. Abstract data structures are ways we can hide information from users that they do not need, also hides the backend of how these operations are ran to make a better user experience, can catch errors easier, and can be made into more flexible programming.

## Prompt 4

A few classic problems involving a stack are the `isBalanced` and `isPalindrome` functions. Choose one of these functions and provide a solution to it along with a brief lesson explaining how it works.

### Response 4
