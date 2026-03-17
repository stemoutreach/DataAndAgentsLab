# Foundations Guide

This guide is the shared starting point for students preparing to work with Python, Jupyter notebooks, data, and AI-assisted problem solving.

It is designed for beginners. The goal is not to memorize everything. The goal is to build enough confidence to:
- work in a Jupyter notebook
- read and modify Python code
- understand basic data
- solve problems step by step
- use AI as a helper without turning off your own thinking

This guide should be completed before moving into either of the two focused paths:
- Classic AI / Machine Learning
- Agentic AI

---

## Learning Goals

By the end of this guide, students should be able to:

- open and use a Jupyter notebook confidently
- run, edit, and re-run code cells
- understand basic Python syntax
- use variables, lists, dictionaries, conditionals, loops, and functions
- read simple code and explain what it is doing
- debug common beginner errors
- understand basic tables and structured data
- read scaffolded notebook tasks with TODO sections
- interpret simple outputs and plots
- break a problem into smaller steps
- use AI to support learning while still checking the results carefully

## Why Foundations Matter

Many students assume the hardest part of AI work is the “AI” itself.

Usually, that is not true.

The hardest part is often:
- understanding the task
- following instructions carefully
- reading code
- testing changes
- recognizing mistakes
- knowing whether a result makes sense

Strong foundations make everything else easier.

## Part 1: Working in a Jupyter Notebook

### What a Jupyter Notebook Is

A Jupyter notebook is an interactive coding workspace made of cells. Some cells contain code. Some contain text, directions, or questions.

Students should know how to:
- click into a cell
- edit code
- run a cell
- read output
- move between cells
- tell the difference between code and explanation text

### Skills to Build

- running one cell at a time
- understanding that cells often depend on earlier cells
- re-running a cell after making a change
- noticing whether output changed
- restarting and re-running when the notebook gets out of sync

### Worked Example: Cell Order

```python
points = 5
bonus = 2
total = points + bonus
print(total)
```

Expected output:

```python
7
```

What to notice:
- this code depends on `points` and `bonus` being defined first
- if you run a later cell before these variables exist, the notebook can fail
- notebook order matters

## Part 2: Python Basics

Students should understand:
- strings, integers, floats, and booleans
- lists and dictionaries
- conditionals
- loops
- functions
- printing values to inspect their work

### Example

```python
def greet(name):
    return f"Hello, {name}!"

names = ["Ava", "Luis", "Mia"]

for name in names:
    print(greet(name))
```

Expected output:

```python
Hello, Ava!
Hello, Luis!
Hello, Mia!
```

What to notice:
- the function is reused three times
- the loop sends each name into the function
- the output pattern helps confirm the code is working

## Part 3: Reading and Debugging Code

Students do not need to write everything from scratch to be successful. But they do need to read code and understand what is happening.

### Skills to Build

- read code from top to bottom
- identify inputs
- identify outputs
- track how a variable changes
- explain what a loop is doing
- explain what a function returns
- test one change at a time

### Common Beginner Errors

- Syntax errors
- Name errors
- Type errors
- indentation mistakes
- forgetting to run earlier cells

### Worked Example: Reading an Error

Broken code:

```python
message = "Hello
print(message)
```

Example error:

```python
SyntaxError: unterminated string literal
```

What it means:
- Python found the start of a string but never found the closing quote

Fixed code:

```python
message = "Hello"
print(message)
```

Expected output:

```python
Hello
```

### Good Debugging Habits

- read the error message carefully
- look at the line number
- inspect nearby code
- print values to see what they contain
- change one thing at a time
- re-run the relevant cells

## Part 4: Data Basics

Students should understand:
- rows are records or examples
- columns are features or fields
- each cell contains one value
- data may be missing, messy, or inconsistent

Helpful beginner tasks:
- load data
- look at the first few rows
- inspect column names
- count rows
- describe simple patterns

### Worked Example: Reading a Table

```python
import pandas as pd

df = pd.DataFrame({
    "machine": ["M-101", "M-102", "M-103"],
    "temperature": [71.2, 89.7, 73.4],
    "status": ["normal", "review", "normal"]
})

print(df.head())
```

Expected output:

```python
  machine  temperature  status
0   M-101         71.2  normal
1   M-102         89.7  review
2   M-103         73.4  normal
```

What to notice:
- each row is one machine reading
- each column stores one kind of information
- the second row already looks interesting because its status is `review`

## Part 5: Reading Challenge-Style Notebook Tasks

Many challenge notebooks include starter code, examples, hints, and TODO sections.

Students should practice:
- reading the full instruction before changing code
- locating exactly what is supposed to be edited
- preserving important variable names
- avoiding edits to setup code unless told to change it
- checking what type of output is expected

### Worked Example: TODO Repair

Starter code:

```python
def double_value(x):
    # TODO: fix this line
    return x + 2

print(double_value(4))
```

Expected output should be:

```python
8
```

Fixed code:

```python
def double_value(x):
    return x * 2

print(double_value(4))
```

What to notice:
- only one line needed to change
- reading the expected output helps you know what to fix
- challenge notebooks often work this way

## Part 6: Simple Plotting and Interpretation

Students do not need advanced visualization skills, but they should be able to:
- read a basic chart
- explain what it shows
- notice unusual values
- use a simple plot to inspect data

Examples of beginner-friendly visuals:
- bar charts
- line plots
- histograms
- scatter plots

## Part 7: Problem-Solving Basics

A simple problem-solving process:

1. Read the task carefully
2. Identify the inputs
3. Identify the output
4. Break the task into smaller parts
5. Test as you go
6. Compare expected vs actual

## Part 8: Using AI Well While Learning

AI can be a powerful assistant. But it is not a replacement for thinking.

**AI helps generate. Humans must decide.**

Students can use AI to:
- ask what an error message means
- ask for an explanation of a Python concept
- request a simpler explanation of code
- ask for help breaking a task into steps
- compare two possible approaches
- get help debugging after trying on their own

Students should avoid:
- blindly copying answers without reading them
- pasting large problems and trusting the first response
- submitting code they cannot explain
- assuming AI output is correct because it sounds confident

## Suggested Practice Checklist

Students should be able to do most of the following before moving on:
- run Jupyter notebook cells in order
- explain what a variable is
- use a list and a dictionary
- write a simple `if` statement
- write a simple `for` loop
- define and call a function
- read a short code block and explain it
- fix a basic syntax or name error
- load simple tabular data
- describe what rows and columns mean
- read a TODO-style notebook cell without getting lost
- explain a simple plot
- break a problem into steps
- use AI to ask for help without blindly copying answers
