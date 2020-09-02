## Call Stack

A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function. Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
If the stack takes up more space than it had assigned to it, it results in a “stack overflow” error.

## what happens when the code is run:

When secondFunction() gets executed, an empty stack frame is created. It is the main (anonymous) entry point of the program.

secondFunction() then calls firstFunction()which is pushed into the stack.

firstFunction() returns and prints “Hello from firstFunction” to the console.

firstFunction() is pop off the stack.

The execution order then move to secondFunction().

secondFunction() returns and print “The end from secondFunction” to the console.

secondFunction() is pop off the stack, clearing the memory.

## Types of error messages
1. Reference errors:

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

1. Syntax errors:

I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

1. Range errors:

Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

1. Type errors:

Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.