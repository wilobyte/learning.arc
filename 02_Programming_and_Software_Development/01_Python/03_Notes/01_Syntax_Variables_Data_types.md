# 01_Syntax_Variables_Data_types

**Date:** 2025-07-31  
**Subject:** Programming  
**Parent MOC:** [[02_Programming_and_Software_Development/01_Python/00_MOCs/02_Data_Types_Variables_and_Operators_MOC|02_Data_Types_Variables_and_Operators_MOC]]  
**Language/Topic:** {{python}}
**Source / Reference:**  [Automate the boring stuff](obsidian://open?vault=learning.arc&file=02_Programming_and_Software_Development%2F01_Python%2F01_Resources%2F01_Automate_the_Boring_Stuff_with_Python_Sweigart_.pdf)

---

## Learning Objectives  
-  Learn about expressions and how Python evaluates them
- Identify the three main data types in python
- Learn how to store expressions in variables

---

## Concepts and Definitions  
### Expressions
-  The most basic way to interact with the python is through the *interactive shell*. When opened the shell will prompt you to input an expression after the chevron (`>>>`) symbol.
- For example we might enter the following into the interactive shell's prompt to do some simple math:  
	```python
	>>> 2 + 2
	4
	```
- An *expression* is the most basic kind of programming instruction in the language. It comprises the *values* (such a `2`) and the *operators* (such as `+`), which will always *evaluate* (break down) to a single value. In the previous example, `2 + 2` evaluates to a single value, `4`. 
- A single value without an operator is considered to be an expression, though it only evaluates to itself like shown:
	```python
	>>> 2
	2
	```
- There are numerous operators you can use in Python expressions. The following is the list of all the math operators in python:
	
	| Operator | Operation                         | Example  | Evaluates to... |
	| -------- | --------------------------------- | -------- | --------------- |
	| `**`     | Exponent                          | `5 ** 2` | `25`            |
	| `%`      | Modulus/remainder                 | `5 % 2`  | `1`             |
	| `//`     | Integer division/Floored quotient | `5 // 2` | `2`             |
	| `/`      | Division                          | `5 / 2`  | `2.5`           |
	| `*`      | Multiplication                    | `5 * 2`  | `10`            |
	| `-`      | Subtraction                       | `5 - 2`  | `3`             |
	| `+`      | Addition                          | `5 + 2`  | `7`             |
- The *precedence* (order of operations) of math operations in Python is similar to that of mathematics. The `**` is evaluated first; followed by the `*`, `/`, `//`, and `%` operators in that order from left to right; and the `+` and `-` operators are evaluated last (also from left to right). You can use parentheses to override the usual precedence if you need to (since everything in parentheses like this text is evaluated first).
- Example of parentheses override:
	```python 
	>>> 2 * 6 + 3
	15
	>>> 2 * (6 + 3)
	18
	```
- The rules for putting together values and operators to form an expression is a fundamental part of the Python programming language, just like grammar rules that help us to communicate. For example:
	
	**This is a grammatically correct English sentence.**
	**This grammatically English sentence correct is a.**

	The second line is difficult to parse because it does not follow the rules of English. Similarly, if you type in an incorrect expression, Python will not be able to understand it and will respond with a `SyntaxError` error message.
- Syntax error example:
	```python
	>>> 5 +
	  File "<python-input-6>", line 1  
	   5 +  
	      ^  
	SyntaxError: invalid syntax  
	```

### Data Types: Integer, Floating-Point, and String
- Data types are a way to categorize the values in an expression, and every value belongs to exactly one data type.
- The table below shows the most common data types in python:
	
	| Data type              | Examples                                    |
	| ---------------------- | ------------------------------------------- |
	| Integers               | `-2, -1, 0, 1, 2`                           |
	| Floating-point numbers | `3.3, -2.4, 1.0, 0.0`                       |
	| Strings                | `'a', 'aa', 'Suspiciously holding a salmon` |
- The integer (or *int*) indicates values that are whole numbers.
- The floating point numbers (or *floats*) indicate numbers with a decimal point.
- Strings or *strs* (pronounced "stirs") indicate text values. Always surround your string in single quote (') characters. You can even have a string with no characters in it, `''`, this is called a *blank string*.
- Note that even though `42` is an integer number, the value `42.0` would be a floating point number.
- If you see the error message `SyntaxError: unterminated string literal`, you probably forgot to close the quotes around the string, such as in the below example:
	```python
	>>> 'Hello terra!  
	File "<python-input-0>", line 1  
	   'Hello terra!  
				    ^  
	SyntaxError: unterminated string literal (detected at line 1)  
	```

- ### String Concatenation and Replication
	- The meaning of an operator may change depending on the data type it is operating on. For example, `+` is the addition operator for integers and floating-point values. However, when `+` is used, it refers to the *string concatenation operator* as shown below:
		```python
		>>> 'Sassy' + 'Shellfish'  
		'SassyShellfish'
		```
	- The expression evaluates down to a single value which is a new string that combines the text of the two strings. 
	- However if you try to use the `+` operator on a string and integer value, Python won't know how to parse this, and it will display an error message
		```python
		>>> 'life' + 42  
		Traceback (most recent call last):  
		 File "<python-input-3>", line 1, in <module>  
		   'life' + 42  
		   ~~~~~~~^~~~  
		TypeError: can only concatenate str (not "int") to str
		```
	- If you'd like to add both an integer and string value like in a date "February 19", your code will have to explicitly convert the integer value to a string, because Python cannot do this automatically.
	- The `*` operator multiplies two integer of floating-point values. But when the `*` operator is used on one string value and one integer value, it becomes the *string replication* operator.
		```python
		>>> 'cars' * 3  
		'carscarscars'
		```
	- The expression evaluates down to a single value that repeats the original a number of times equal to the integer value.
	- The `*` operator can only be used with two numeric values (for multiplication) or one string value and one integer value (for string replication). Otherwise, Python will just display an error message.
		```python
		>>> 'cars' * 'kachow'  
		Traceback (most recent call last):  
		 File "<python-input-5>", line 1, in <module>  
		   'cars' * 'kachow'  
		   ~~~~~~~^~~~~~~~~~  
		TypeError: can't multiply sequence by non-int of type 'str'  
 		>>> 'cars' * 5.0  
		Traceback (most recent call last):  
		 File "<python-input-6>", line 1, in <module>  
		   'cars' * 5.0  
		   ~~~~~~~^~~~~  
		TypeError: can't multiply sequence by non-int of type 'float'
		```
- ### Storing Values in Variables
	- A variable is like a container in the computer's memory where you can store a single value. If you want to use the result of an evaluated expression later in the program, you can store it in a variable.
	- #### Assignment Statements
		- An *assignment statement* is used to store a single value in a variable.
		- An assignment statement contains the variable name, an equal sign (called the assignment operator), and the value to be stored. If you enter the assignment statement `life = 41`, then a variable named `life` will have an integer value `41` stored in it.
		- Here's an example:
			```python
			>>> life = 41 
 		    >>> life  
			41  
 		    >>> garri = 6  
 		    >>> garri + life  
			47  
 		    >>> garri + garri + life  
			53  
 		    >>> life = life + 2  
 		    >>> life  
			43
			```
		- A variable is *initialized* (or created) the first time a value is stored in it.
		- After that, you can use it in expressions with other variables and values.
		- When a variable is assigned a new value, the old value is forgotten, which is why `life` evaluated as `43` instead of `41` at the end of the example. This is called *overwriting* the variable.
	- #### Variable Names
		- A legal variable name must follow the following rules:
			- It can only be one word.
			- It can use only letters, numbers, and the underscore ( _ ) character.
			- It can't begin with a number.
		- Variable names are case sensitive, so `life` is different from `LIFE` as well as `Life`, and these are all 3 different variables.

- ### Analyzing the Code Snippet 
	- #### Comments
		- Python totally ignores comments and does not evaluate them.
		- They are used by putting a hash mark (#) followed by any value which python will ignore.
			```python
			# This is a comment. lalalalalalalala
			```
		- You can use them to highlight, or document parts of code. You can also use them to remove lines of code for debugging or testing, commonly called *commenting out* the code.
		- Python also ignores the blank line after the comment. You can use this to arrange your code in a paragraph-esque structure.
	- #### The print() Function
		- The `print()` function displays the string value stored in the parentheses on the screen.
			```python
			print('Hello th1s is a string of characters!')
			```
		- The line `print('Hello th1s is a string of characters!)` means "Print out the characters in the string value `'Hello th1s is a string of characters!'`"
		- When Python executes this line, you say that Python is *calling* the `print()` function and the string value is being *passed* to the function. A value that is passed to a function call is called an *argument*.
		- Notice that the quotes aren't printed to the screen; this is because the quotes just indicate that the characters in it are the entire string value. This helps Python identify what is a string value.
		- You can also use this function to print a blank line. You can achieve this by leaving the parentheses in the function empty during the function call.
		- When writing a function name, the opening and closing parentheses at the end indicate it as the name of a function.
	- #### The input() Function
		- The `input()` function waits for the user to type some characters on the keyboard and press `ENTER`.
			```python
			myName = input()
			```
		- This function call evaluates to a string value that is equal to the characters entered in by the user. The previous line of code stores assigns string value to the variable `MyName`
	- #### The len() Function
		- You can pass the`len()`function a string value (or a variable containing a string) and the `len()` function will evaluate the integer value of the characters in that string.
			```python
			>>> len('mulberry street, so good to see you')  
			35
			>>> len(' ')  
			1  
 			>>> len ('')  
			0
			```
	- #### The str(), int(), and float() Functions
		- If you want to concatenate an integer value like `5` with a string and pass it to the `print()` function, you'll need to get the value `'5'` which is the string form of `5`.
		- The `str()` function can be passed an integer value an with evaluate to a string value version of it.
		- **The `str()`, `int()`, and `float()` functions will evaluate to the string, integer, and floating point forms of the value you pass, respectively.**
		- Note that the `input()` function always returns a string so you can pass this string value to the `int()` function if you want to do some mathematics.
			```python
			>>> myName = input()
			101
 		    >>> int(myName)
			101
			```
		- Now you can treat the `myName` variable as an integer. 
		- If you pass a value to `int()` that it cannot evaluate, Python will display an error message 
			```python
			>>> int('99.99')  
			Traceback (most recent call last):  
			 File "<python-input-0>", line 1, in <module>  
			   int('99.99')  
			   ~~~^^^^^^^^^  
			ValueError: invalid literal for int() with base 10: '99.99'
			```
		- Note, and integer can be equal to a floating point.

---

## Code Snippets / Algorithms  
``` python
# This program says hello and asks for my name.

print('Hello World!')
print('What is your name?')    # ask for their name
myName = input()
print('It is good to meet you ' + myName)
print('The length of your name is:')
print(len(myName))
print('What is your age?')     # ask for their age
myAge = input()
print('You will be ' + str(int(myAge) + 1) + 'in a year.')
```
 
---

## Debugging Notes / Common Issues  
- It seems you can store multiple values in a variable 
	```python
	>>> life = 'jin', 'kaa'  
 	>>> life  
	('jin', 'kaa')  
	>>> print(life)  
	('jin', 'kaa')  
	>>> fun = 'kim', 5  
 	>>> fun  
	('kim', 5)  
 	>>> print(fun)  
	('kim', 5)
	```
- Actually it's just that sending comma separated values to a variable turns it into a **tuple** if it isn't already one.
- Words cannot evaluate with numbers except with the string replication operation

---

## Practice Problems / Exercises  
-  

---

## Projects and Implementations  
- Related project(s):  
  - [Project Name](./Projects/Project_Name/)  

---

## Questions / Review Points  
-  It seems that python changes it's error messages. Why is this done?  `SyntaxError: EOL while scanning string literal` vs `SyntaxError: unterminated string literal`
- Can Python store multiple values in a variable? In what sense?
---

## Links to Related Notes  

---

## Tags  
#programming #{{topic}} #code #to-review
