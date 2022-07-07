# notes.md / Introduction to Python Programming
Author: Elia Deppe  
Editor: ...  

## Variables and Assignment Statements

What are variables?
>

What are the legal character(s) or character sets for variable names?  
> 1. ...
> 2. ...
> 3. ...

The creation of a variable is considered to be a ...?
> 

When creating variables, what operator do you use to assign a value to it? What is the name of the operator?
>

### Code  
Create 4 Variables below according to the following specifications:  
1. Create a variable to hold a number.
2. Create a variable to hold a number greater than 1000.
3. Create a variable to hold a negative number.
4. Create a variable to hold a float.

How do you get the data type of a variable?
> 

What are the two data types for numbers?  
> 1. ... 
> 2. ...


## Arithmetic  
The following table summarizes arithmetic operators, which include some symbols not used in algebra.  

| Python Operation   | Arithmetic Operator | Algebraic Expression  | Python Expression |
|--------------------|---------------------|-----------------------|-------------------|
| Addition           | +                   | _f + 7_               | f + 7             |
| Subtraction        | -                   | _p - c_               | p - c             |
| Multiplication     | *                   | _b × m_ or _b • m_    | b * m             |
| Exponentiation     | **                  | _x<sup>4</sup>_       | x ** 4            |
| True Division      | /                   | _x / y or x ÷ y_      | x / y             |
| Floor Division     | //                  | _⌊x / y⌋ or ⌊x ÷ y⌋_  | x // y            |
| Remainder (Modulo) | %                   | _r mod s_             | r % s             |

What is the order of operation precedence?  
> 1. ...
> 2. ...
> 3. ...
> 4. ...

What is the difference between True Divison and Floor Division? Give an example.
> 

What does the modulo operator do? Why might this be useful?
> 

### Code  
Create 7 variables according to the following specifications.
1. Create a variable that is sum of an addition operation.
2. Create a variable that is the difference of a subtraction operation.
3. Create a variable that is the product of a multiplication operation.
4. Create a variable that is the power of a number.
5. Create a variable that is the quotient of a true division operation.
6. Create a variable that is the quotient of a floor division operation.
7. Create a variable that is the remainder of a division operation.

## Function print() and Strings  

### `print(\*objects, sep=' ', end='\n', file=sys.stdout, flush=False)`  

> Print objects to the text stream _file_, separated by _sep_ and followed by _end_. _sep_, _end_, _file_, and _flush_, if present, must be given as keyword arguments.  
> 
> All non-keyword arguments are converted to strings like `str()` does and written to the stream, separated by _sep_ and followed by _end_. Both _sep_ and _end_ must be strings; they can also be `None`, which means to use the default values. If no objects are given, `print()` will just write _end_.  
> 
> The file argument must be an object with a `write(string)` method; if it is not present or `None`, `sys.stdout` will be used. Since printed arguments are converted to text strings, `print()` cannot be used with binary mode file objects. For these, use `file.write(...)` instead.  
> 
> Whether the output is buffered is usually determined by _file_, but if the _flush_ keyword argument is true, the stream is forcibly flushed.
> 
> Documentation from python.org - https://docs.python.org/3/library/functions.html#print  

### Using `print()`  
Print is primarily used to print something to the screen, or the console more specifically. This is useful for outputting information to the user. Here are some examples with `print()`:  
```python
# Printing a number:
print(45)

# Printing the result of an operation:
print(2 - 7 + 14)

# Printing a variable:
x = 5
y = 10
print(x)
print(x * y)
```

### Printing Text  
In Python, we can print text using strings. A string is surrounded by either quotation symbols `"like this"` or apostrophe symbols `'like this'`. **The starting symbol must be the same as the closing symbol.**  
```python
# Printing some text:
print('Hello!')
print('I am printing some text here!')
print('Pretty simple right?')
```

### Printing Multiple Objects  
When printing a single number, string, variable, or result of an operation; that is considered to be one object. We are allowed to print multiple objects by seperating them with commas.

```python
# Printing multiple string objects:
print('these', 'strings', 'are', 'all', 'different', 'objects!')

# You can also print multiple numbers / operations:
print(10, 24, 45 % 3)
```

### Strings and Variables  
As a note, strings, like integers or floats, can be saved to a variable:
```python
name = 'elia deppe'
birthday = '10/21/1995'
```

### Escape Sequences  
Escape sequences are a sequence of characters that does not represent itself when used inside a character or string literal, but is translated into another character or a sequence of characters that may be difficult or impossible to represent directly.  

| Escape Sequence | Description                                                                                                                                       |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| \n              | Insert a newline character in a string. When the string is displayed, for each newline, move the screen cursor to the beginning of the next line. |
| \t              | Insert a horizontal tab. When the string is displayed, for each tab, move the screen cursor to the next tab stop.                                 |
| \\\\            | Insert a backslash character in a string.                                                                                                         |
| \\"             | Insert a double quote character in the string.                                                                                                    |
| \\'             | Insert a single quote character in the string.                                                                                                    |

```python
print('I\nam\nprinting\na\nnew\nword\neach\nline.')
```

### Code  
Write the following statements according to the specifications:  
1. Print your name.
2. Print a line from a book, song, or movie you like.
3. Credit the book, song, or movie by printing the title and the author or director. Seperate these into two objects.
4. Using escape sequences, print 5 animals; each on a new line while only using one print statement.

## Triple Quoted Strings  
Triple Quoted Strings begin and end with three double quotes (""") or three single quotes ('''). It is recommended that you use these for:  
1. ...
2. ...
3. ...

## Getting Input from the User
The built-in **input function** requests and obtains user input: 
```
>>> name = input('What\'s your name?')
What's your name? Elia

>>> name
'Elia'

>>> print(name)
Elia
```

### `input([prompt])` 
> If the prompt argument is present, it is written to standard output without a trailing newline. The function then reads a line from input, converts it to a string (stripping a trailing newline), and returns that. When EOF is read, EOFError is raised.  

### `input()` Always Returns a String  
Functions are essentially operations, which result in a value. This value is then used in the functions place in code. Take the following code for example:  
```
>>> num1 = input('enter the first number: ')
enter the first number: 21

>>> num2 = input('enter the second number: ')
enter the second number: -5

>>> num1 + num2
'21-5'
```

### Converting Input to a Number
Rather than adding together num1 and num2 as integers, they are added together as strings. Strings when added together simply connect to each other end to end. If we want to add these objects from input as integers (or floats), you would need to use type-casting. This is done via casting functions: `int()` and `float()`.  
```
>>> num = input('enter a number: ')
enter a number: 15

>>> num
'15'

>>> num = int(num)
>>> num
15
```

We can do this in one line as well:  
```
>>> num1 = int(input('enter the first number: '))
enter the first number: 10

>>> num2 = int(input('enter the second number: '))
enter the second number: 15

>>> num1 + num2
25
```  
Note that the `int()` functions parenthesis surround the entirety of the `input()` function.  

## Decision Making: The if Statement and Comparison Operators  
What is a **condition?**  
> 

Here are some comparisons being done. Note that the result is always either `True` or `False`.
```
>>> 5 > 7
False

>>> 20 == 20
True

>>> 11 <= 2
False
```

### Comparison Operators  
| Algebraic Operator | Python Operator | Sample Condition | Meaning                         |
|--------------------|-----------------|------------------|---------------------------------|
| >                  | >               | x > y            | x is greater than y             |
| <                  | <               | x < y            | x is less than y                |
| ≥                  | >=              | x >= y           | x is greater than or equal to y |
| ≤                  | <=              | x <= y           | x is less than or equal to y    |
| =                  | ==              | x == y           | x is equal to y                 |
| ≠                  | !=              | x != y           | x is not equal to y             |  

### Making Decisions with the if Statement  
What is the purpose of an if Statement?

```python
num1 = int(input('enter the first number: '))
num2 = int(input('enter the second number: '))

if num1 == num2:
    print(num1, 'is equal to', num2)
    
if num1 != num2:
    print(num1, 'is not equal to', num2)

if num1 > num2:
    print(num1, 'is greater than', num2)

if num1 >= num2:
    print(num1, 'is greater than or equal to', num2)
    
if num1 < num2:
    print(num1, 'is less than', num2)
    
if num1 <= num2:
    print(num1, 'is less than or equal to', num2)
```

What are some things you notics about the structure of an if Statement?
> 1. ...
> 2. ...
> 3. ...

What happens if you don't indent the body of an if statement?
> 

Why do we use if Statements?
> 

### Chaining Comparisons
We can chain comparisons in a similar way we've seen with Math to created a bounded limit. See the following example:

```python
num1 = 10

if 5 < num1 < 15:
    print(num1, 'is greater than 5 and less than 15')
```

### Code
Write the following code segment according to the specifications:
1. Create two variables, num1 and num2, and set them equal to the input from the user.
2. Compare the variables with each other, using every comparison operator in a different if Statement.
   1. You should have a total of 6 if statements.
3. Using comparison operators, find if:
   1. num1 is positive.
   2. num2 is negative.
   3. If num1 is within the range of 0 - 100, inclusive.
   4. If num2 is within the range of -500 to -1000 exclusive.

## Project
In data science, you'll often use statistics to describe and summarize your data. Here, we begin by introducing several such descriptive statistics, including:  
1. minimum - the smallest value in a collection of values.
2. maximum - the largest value in a collection of values.
3. range - the range of values from the minimum to the maximum.
4. count - the number of values in a collection.
5. sum - the total of the values in a collection.

For now, we are going to focus on minimum and maximum values.

Write your project according to the following specifications:
1. Create 5 variables that retrieve input from the user in the form of a number.
   1. These numbers can be integers or floats, your decision.
2. Using these 5 variables find the following:
   1. The minimum value.
   2. The maximum value.
   3. Bonus:
      1. The minimum absolute value.
      2. The maximum absolute value.

For the purposes of this project, you may not use the max() and min() functions, though you may use the abs() function.

Please anser the following questions:
1. We've seen that n = 42 is legal. What about 42 = n?
   1. ...
2. Is x = y = 1 legal?
   1. ...

For the following questions, practice using the Python Console as a calculator:  
1. The volume of a sphere with radius r is equal to (4/3) × π × r<sup>3</sup>, where π is equal to 3.14. What is the volume of a sphere with radius 5.  
   1. 
2. Suppose the cover price of a book is $24.95, but bookstores get a 40% discount. Shipping coses $3 for the first copy, and $0.75 for each additional copy. What is the total wholesale cost for 60 copies?  
   1. 
3. If I leave my house at 6:52 am and run 1 mile at an easy pace, 8 minutes and 15 seconds per mile, then 3 miles at tempo, 7 minutes and 12 seconds per mile, and finally 1 mile at an easy pace again, what time do I finish running?  
   1. 
