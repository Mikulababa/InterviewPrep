# Stack
## Stack
* A stack is a linear data structure in which elements can be inserted and deleted only from one side of the list, called the top. It follows the LIFO (Last In First Out) rules
* LIFO (Last In First Out) means the last added item will be poped out first.

## Application of Stack Data Structure
+ Function calls and recursion: When a function is called, the current state of the program is pushed onto the stack. When the function returns, the state is popped from the stack to resume the previous function’s execution.
+ Undo/Redo operations: The undo-redo feature in various applications uses stacks to keep track of the previous actions. Each time an action is performed, it is pushed onto the stack. To undo the action, the top element of the stack is popped, and the reverse operation is performed.
+ Expression evaluation: Stack data structure is used to evaluate expressions in infix, postfix, and prefix notations. Operators and operands are pushed onto the stack, and operations are performed based on the stack’s top elements.
+ Browser history: Web browsers use stacks to keep track of the web pages you visit. Each time you visit a new page, the URL is pushed onto the stack, and when you hit the back button, the previous URL is popped from the stack.
+ Balanced Parentheses: Stack data structure is used to check if parentheses are balanced or not. An opening parenthesis is pushed onto the stack, and a closing parenthesis is popped from the stack. If the stack is empty at the end of the expression, the parentheses are balanced.
+ Backtracking Algorithms: The backtracking algorithm uses stacks to keep track of the states of the problem-solving process. The current state is pushed onto the stack, and when the algorithm backtracks, the previous state is popped from the stack.

## Advantages
+ Easy implementation: Stack data structure is easy to implement using arrays or linked lists, and its operations are simple to understand and implement.
+ Efficient memory utilization: Stack uses a contiguous block of memory, making it more efficient in memory utilization as compared to other data structures.
+ Fast access time: Stack data structure provides fast access time for adding and removing elements as the elements are added and removed from the top of the stack.
+ Helps in function calls: Stack data structure is used to store function calls and their states, which helps in the efficient implementation of recursive function calls.
+ Supports backtracking: Stack data structure supports backtracking algorithms, which are used in problem-solving to explore all possible solutions by storing the previous states.
+ Used in Compiler Design: Stack data structure is used in compiler design for parsing and syntax analysis of programming languages.
+ Enables undo/redo operations: Stack data structure is used to enable undo and redo operations in various applications like text editors, graphic design tools, and software development environments.

## Disadvantages
+ Limited capacity: Stack data structure has a limited capacity as it can only hold a fixed number of elements. If the stack becomes full, adding new elements may result in stack overflow, leading to the loss of data.
+ No random access: Stack data structure does not allow for random access to its elements, and it only allows for adding and removing elements from the top of the stack. To access an element in the middle of the stack, all the elements above it must be removed.
+ Memory management: Stack data structure uses a contiguous block of memory, which can result in memory fragmentation if elements are added and removed frequently.
+ Not suitable for certain applications: Stack data structure is not suitable for applications that require accessing elements in the middle of the stack, like searching or sorting algorithms.
+ Stack overflow and underflow: Stack data structure can result in stack overflow if too many elements are pushed onto the stack, and it can result in stack underflow if too many elements are popped from the stack.
+ Recursive function calls limitations: While stack data structure supports recursive function calls, too many recursive function calls can lead to stack overflow, resulting in the termination of the program.

## Call Stack
+ Call stack is a stack data structure that stores information about the active subroutines of a computer program. This kind of stack is also known as an execution stack, program stack, control stack, run-time stack, or machine stack, and is often shortened to just "the stack".
+ The main purpose of the Call Stack is to keep track of the point to which each active subroutine should return control when it finishes executing.
  1. Function call management: Whenever a program executes a function call, the relevant information about that function (such as local variables, parameters, and return address) is pushed onto the stack. This allows the program to return to the correct location after the function has completed its execution.
  2. Storage for local variables: Each function is allocated a portion of memory on the stack to store its local variables. These local variables are only visible and accessible within the scope of the function and are automatically deallocated when the function returns.
  3. Support for recursion: The call stack also supports the execution of recursive functions because each recursive call creates a new function call frame on the stack, maintaining the stack's structure.
  4. Exception handling: When an exception occurs in a program, the stack can be used to trace the location of the exception and the call stack's information, aiding in debugging and error handling.
