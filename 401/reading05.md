# Reading05: Linked Lists

##### Linear data structures

One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed. We can think of a linear data structure like a game of hopscotch: in order to get to the end of the list, we have to go through all of the items in the list in order, or sequentially. Linear structures, however, are the opposite of non-linear structures. In non-linear data structures, items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.

##### Memory management

The biggest differentiator between arrays and linked lists is the way that they use memory in our machines. Those of us who work with dynamically typed languages like Ruby, JavaScript, or Python don’t have to think about how much memory an array uses when we write our code on a day to day basis because there are several layers of abstraction that end up with us not having to worry about memory allocation at all.
But that doesn’t mean that memory allocation isn’t happening! Abstraction isn’t magic, it’s just the simplicity of hiding away things that you don’t need to see or deal with all of the time. Even if we don’t have to think about memory allocation when we write code, if we want to truly understand what’s going on in a linked list and what makes it powerful, we have to get down to the rudimentary level.
