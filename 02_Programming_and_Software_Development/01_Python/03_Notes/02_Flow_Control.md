# 02_Flow_Control

**Date:** 2026-01-12  
**Subject:** Programming  
**Parent MOC:** [[03_Control_Flow_Conditionals_and_Loops_MOC]]
**Language/Topic:** {{topic}}  
**Source / Reference:**  

---

## Learning Objectives  
- Boolean Values
- Comparison Operators
- Boolean Operators
- Flow Control Statements

---

## Concepts and Definitions  
- ### Boolean Values
	- This particular data type can only have two values: `True` or `False`.
	- Named after the mathematician George Boole, thus being capitalized.
	- The Boolean data types lack any quotes that you place around strings and always start with a capital *T* or *F*, followed by lower case to complete the word.
	- Boolean values can be used in expression and can be stored in variables just like any other value. 
	- Note that if you don't use proper case, or try to name variables `True` or `False`, Python will greet you with an error.
- ### Comparison Operators
	- Comparison operators compare two values and evaluates down to a single **Boolean** value.
	- Comparison operators are shown in the table below. They evaluate to `True` or `False` depending on the values given to them.

		| Operator | Meaning                  |
		| -------- | ------------------------ |
		| ==       | Equal to                 |
		| !=       | Not equal to             |
		| <        | Less than                |
		| >        | Greater than             |
		| <=       | Less than or equal to    |
		| >=       | Greater than or equal to |
	- `==` evaluates to `True` when both values on both sides are the same.
	- `!=` evaluates to `True` when they are different.
	- Both `==` and `!=` can work with any values of any data type.
	- The integer and floating point value will always be unequal to a string value. `42` and `'42'` cannot be equal, because Python considers the string `'42'` to be different from the integer `42`.
	- The `<`, `>`, `<=`, and `>=` operators, on the other hand, work properly only with integer and floating point values.
- ### Boolean Operators
	- We have three Boolean operators (`and`, `or` and `not`) and these are used to compare Boolean values.
	- Like comparison operators, these evaluate down to a single Boolean value.
	- #### Binary Boolean Operators
		- The `and` and `or` operators always work with two Boolean values (or expressions), hence they are called *binary* operators.
		- The `and` operator evaluates an expression to `True` if *both* Boolean values (or expressions) are `True`; otherwise it evaluates to `False`.
		- On the other hand, the `or` operator evaluates to `True` if either of the Boolean values are `True`.
		- Unlike the `and` and `or` operators, the `not` operator operates on only one Boolean value (or expression) and evaluates to the opposite Boolean value.
- So essentially conditions are statements that can evaluate to a single (Boolean) value and based on the value of these conditions you can use these with statements to execute blocks of code.
- The first part of flow control statements contain the condition then the block of code called the clause
- A block of code starts with indentiation, basically you can see it
- After the condition there's a colon `:` and aftr that and indented block of code
- An if statement only executes the block of code if the condition is true.
- Code is executed like a book (python at least) where it just runs from top to bottom ocassionally chechks then exits
- After the if statement, you can specify an else statement that will only run if the if statement is false.
- elif can be used to check multiple conditions following an if statement and also other elif statements, it will only check/evaluate if the previous statement is false
- also after the check is considered as true no other statements are checked
- you should keep in mind the order of elif statements so you ensure the proper order of checks for example, if i was checking if someone is grater than 12 or 2000, and i say okay is your age older than that 2000 then youre old if that is true, if the 12 elif comes first the custom message for the greater than 2000 range wouldnt work. I know this example doesnt sound good but idc
- adding an else statement after an elif statement guarantees one of the blocks will run
- While loop statements are similar to if statements with the which keyword followed by a conditon, colon and block of code, the behaviour is different with when it reaches the end of the code block it loops back to the while statement and continues looping until the statement evaluates to false
- break statement breaks the loop earlier wherever it's found in the block
- continue statements jump back to the start of the loop
- you can use ctrl c to break an infinite loop in the terminal if stuck
- for statements loop only a certain number of times, can be used in conjuction with the range function e.g `for i in range(5)`, so essentially it updates the nuber in every loop which can be used in the loop as well, in this case the variable containing the number is called `i`. the range starts counting from 0 so the max  value of i will be 4 i.e 0,1,2,3,4
- you can use the break and continue statements in the for loops as well, note however that you can only use the statements in while and for loops
- the range function can accept 3 arguments first the start (first digit), stop (the last digit to stop at i.e it doesnt include it) and the step to be the amount each repetiton is added i.e a step of 2 would be 0,2,4,6..., you can also use negative numbers 
- you can import modules that contain special funtions from the python standard library by using the `import module` for example theres a math module and a random module, to use the funtions in these modules you jsut imported use module.function()
- you can import a lot in one line by using comma separation e.g `import os, math, random` 
- you can also import functon like so `from module import *` this imports all funcitons and it doesnt need the `module.` prefix
- you can end a program early with the sys.exit() function.




---

## Code Snippets / Algorithms  
``` python
# Boolean Values
>>> josh = True
>>> josh
True
>>> true

# Comparison operators
>>> 'rain' == 'rain'
True
>>> 'rain' == 'Rain'
False
>>> 42 == 49
False
>>> 42 == 42.0
True
>>> 4 != 8
True
>>> 9 > 0
True
>>> universe = 42
>>> universe >= 42
True

# Boolean operators
>>> True and True
True
>>> False and True
False
>>> False and False
False
>>> False or True
True
>>> False or False
False
>>> True or True
True
>>> not True
False
>>> not False
True
>>> 
```
 
---

## Debugging Notes / Common Issues  
-  

---

## Practice Problems / Exercises  
-  

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
