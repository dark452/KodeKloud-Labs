# Python Comments

1.- Which character is used in Python to make a single-line comment?

```python
#
```

2.- What is the output of the following python code?

```python
name = "Sally" # employee name 
address = "101 Main St, Apt. #100"  
print(name, "address:", address)
```

Answer:
Sally address: 101 Main St, Apt. #100

3.- A comment in Python starts with the hash character #, and extends to the end of the physical line.

A: True

4.- What are comments used for in Python?

A: To ignore code so that it does not execute

5.- What is the output of the following Python code?

```python
# x = 5
# y = 6
z = 7
print(x+y+z)
```
A: NameError (NameError: name 'x' is not defined)

6.- You can use Python comments on independent lines, or on multiple lines to include larger documentation.

A: True

7.- According to PEP8, there must always be a single space after the character `#` for comments. Also, when we have inline comments, those should be separated by at least two spaces from the code. They should start with a `#` and a single space.

Be very economic with inline comments as they tend to distract if they state the obvious.

From the PEP8 examples:

Don’t do this:

```python
x = x + 1  # Increment x
```

But sometimes, this is useful:

```python
x = x + 1  # Compensate for border
```

Ref: https://pep8.org/#comments

Which of the following coding styles is correct?

A: apples = 5 # total number of apples

8.- Which of the following comments might make sense and not be redundant in a program?

A: var /= 5 # this is a shortcut operation

9.- In the file `book.py`, two lines of code produce errors and undesirable results. Get rid of these lines to debug it.


The print result should be: `Does publisher O'Reilly have a book called 'Python Basics'?`

A:

```python
book = "'"
book += "Python Basics"
publisher = "O'Reilly"

print("Does publisher", end=" ")
print(publisher, end=" ")
print("have a book called", book, end="'?")
```

```bash
python3 book.py
Does publisher O'Reilly have a book called 'Python Basics'?
```

10.- Comments should be always indented the same as the code they explain and should be written before the code they explain.

Did you know? On code execution, whenever Python encounters a comment, it perceives it as one space no matter how long the comment is.

In the file `layout.py`, there are too many comments about the variables and the purpose of the program. Make the code more readable!

```python
# The top of the page
top = 20

# The height of the page
page_height = 800

# Space between text and images
padding = 5

# The height of the image
height = 600

# The caption of the image
caption = "flowers"

# Calculate the position of the caption.
position = top + height + padding

# Print the message that indicates where the caption should be placed.
print("Image caption", caption, "to be placed at", position, "pixels height from top of the page")
```