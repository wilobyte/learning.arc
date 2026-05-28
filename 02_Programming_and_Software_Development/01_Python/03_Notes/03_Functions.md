
# 03_Functions

**Date:** 2025-09-15  
**Subject:** Programming  
**Parent MOC:** [[04_Functions_and_Modular_Programming_MOC]]  
**Language/Topic:** {{topic}}  
**Source / Reference:**  

---

## Learning Objectives  
-  Learn about functions.

---

## Concepts and Definitions  
- Basically, a function is like a mini-program within a program.
- ```python
  def function_name():
	  [code block]
  ```
-  To make a function, we use a `def` statement, which defines a function with a given name followed by closed parentheses `function_name()`. 
- The code in the block after the def statement defines what the function does (the body of the function). The code in this block is executed when the function is called not when it is first defined.
- To call a function, just input the name you used in the `def` statement i.e `function_name()` in the interactive shell or in the script.
- A function call is basically the function's name followed by parentheses, possibly with some number or arguments within these parentheses.
- When the code execution reaches a function call, it jumps to the block of code in the function's definition and executes there. After it's done, it returns back to the function call and continues executing the program from there.
- Functions are useful for grouping repetitive blocks of code, to prevent duplication. You'll often find it useful to remove repeated parts of code called *deduplicating*, to make the code easier to read.
- ```python
  def function_name(parameter):
	  [code block(usually containing an expression with the parameter)]
  ```
- Sometimes, we would like to pass arguments to our function to use in evaluation in it's code block. To do this, we need a special variable to store the passed argument(s) to be used in the function's code block. This variable is called a *parameter*.
- Parameters are essentially placeholder variables that store the arguments passed to the function during the function call to be used for evaluation in it's code block.
- N/B: After a function call is evaluated and returns to continue it's execution, the argument's value that was used in the parameter is deleted. If you try to use the parameter name in an expression, an error `NameError`, will be displayed because the variable was destroyed when the function call had returned.
- The value that a function call returns is called a *return value*.
- To make our function return a value of our choosing we use a *return statement*. It's structured as `return *value*`. 
- It's useful to use return statements if we want our function to return specific statements based on specific values.
- Remember, a function call can be used in an expression because it evaluates to it's return value.
- In Python, there is a value called `None`, which represents the absence of a value. It is the only value of the `NoneType` data type. 
- Just like the Boolean values, `None` must be typed with a capital N. One specific use is if we need to store something that won't be confused with a real value in a variable. 
- The `print()` function displays text on the screen, but it doesn't need to return any value in the same way `len()` or `input()` does. But, since all functions need to return a value, `print()` returns `None`.
- ```python
  >>> spam = print('hello')  
      hello  
  >>> spam  
  >>> None == spam  
      True
  ```
- Python returns `None` to any function definition without a return statement.
- If we use a return statement without a value i.e followed by nothing, it returns the `None` value.
- Most arguments are defined by their position in the function call. For example, `random.randint(1,8)` won't return the same value as `random.randint(8,1)` because in the `random.randint()` function, the first argument is the low end of the range and the second is the high end so `random.randint(8,1)` returns an error.
- However, *keyword arguments* depend on the keywords put before them in the function call. They are often used for optional parameters.
- ```python
  function_name(argument, keyword = argument)
  ```
- For example, the `print()` function has the optional parameters `end` and `sep` which specify the characters to be printed at the end of an argument and between (separating) them respectively. By default, the `end` value is a newline and the `sep` value is a space.
- We can modify the optional parameters as so `print('hello', end = '')` to print the blank string at the end. You can do the similar thing with the `sep` keyword as well.
- You can add keywords arguments to functions you write as well, however we'll look into that later on after learning abut the list and dictionary data types.
- Parameters and variables assigned in a called function are said to exist in the function's *local scope*. Variables outside all functions are said to exist in the *global scope*. A variable must be one of the other. It can't be both local and global.
- Think of scopes like containers if it's destroyed, all variables in them are forgotten. For example, the global scope is created when the program is first opened while the local scope is created whenever a function is called. When you close the program the global scope is destroyed and, all variables get forgotten and when the function call returns, all variables in the function get forgotten.
- Reasons why scopes matter:
	- Code in global scope cannot use any local variables.
	- However, a local scope can access global variables.
	- Code in a function's local scope cannot use variables in any other local scope.
	- You can use the same name for different variables if they are in different scopes. (avoid this though)
- The reason why Python has different scopes instead of everything being a global variable is when variables are modified by code in a particular call to a function, the function interacts with the rest of the program only through it's parameters and return value. This helps narrow down the list code lines that might be causing a bug. This helps narrow down the specific scope it's in instead of anywhere in the program. 
- While using global variables in small programs is fine, it becomes a bad habit with larger programs.
- To modify a global variable from within a function, use the *global statement*.
- If you have a line such as `global variable` it tell the function that we are referring to the global variable `variable` that exists in the global scope so don't create a local variable with this name.
- Rules for identifying a variables scope:
	- A variable is global if it exists outside any function's code block.
	- A variable is local if the variable is used in an assignment statement in the function.
	- A variable is global if the variable wasn't used in an assignment statement in the function's code block.
	- If there is a `global` statement for a variable in a function, the variable is global.
- If you try to use a local variable before you assign a variable to it, Python will give you an error because it will never assume that the variable you refer to is global.
- Exceptions are handled by `try` and `exception` clauses. The code in a `try` clause is tested first then if an error occurs in it it jumps the rest of the code in the `try` clause and executes the code in the `except`clause.

---

## Code Snippets / Algorithms  
``` insert code here
```
 
---

## Debugging Notes / Common Issues  
-  

---

## Practice Problems / Exercises  
-  1. Why are functions advantageous to have in your programs?
	- They he;p to avoid redundancy while programming by collecting a block of code that is used repetititvely in the program
2. When does the code in a function execute: when the function is
defined or when the function is called?
	 The code executes when the function is called
3. What statement creates a function?
	a def statement
4. What is the difference between a function and a function call?
	a function is a block of code represented by the name given in it's def statement and it is run only when the function is called.
5. How many global scopes are there in a Python program? How many
local scopes?
	there is only one global scope while the local scope depends on  the number of functons defined
6. What happens to variables in a local scope when the function call returns?
	they are deleted
7. What is a return value? Can a return value be part of an expression?
	a return value is the value returned by the function call. a return value can be used in expressions since it's explicitly a value
8. If a function does not have a return statement, what is the return value
of a call to that function?
	 None
9. How can you force a variable in a function to refer to the global variable?
	by using the global statement
10. What is the data type of None?
	NoneType
11. What does the import areallyourpetsnamederic statement do?
	it imports a module called areallyourpetsnamederic into the python script and allows you to use any function(s) defined in it
12. If you had a function named bacon() in a module named spam, how
would you call it after importing spam?
	spam.bacon()
13. How can you prevent a program from crashing when it gets an error?
	by using try and except blocks 
14. What goes in the try clause? What goes in the except clause?
	the expression(s) to be tested goes into the try block while what to do when the program doesn't run goes into the except block

---

## Projects and Implementations  
- Related project(s):  
  - [Project Name](./Projects/Project_Name/)  

---

## Questions / Review Points  
-  

---

## Links to Related Notes  

---

## Tags  
#programming #{{topic}} #code #to-review
