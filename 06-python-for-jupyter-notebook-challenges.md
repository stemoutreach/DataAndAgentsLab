# Python for Jupyter Notebook Challenges

This guide helps students practice the Python skills that show up often in challenge-style Jupyter notebooks.

The goal is not to memorize every detail. The goal is to become comfortable reading starter code, making focused edits, and finishing notebook tasks without getting lost.

---

## Why This Guide Matters

Many students learn Python basics, but challenge notebooks often require a more practical skill set:
- reading code that is already started
- completing TODO sections
- calling functions with the right inputs
- working with lists and dictionaries
- tracing values through multiple cells
- making small changes without breaking the notebook

## Skills to Practice

Students should be comfortable with:
- variables
- lists
- dictionaries
- loops
- functions
- printing intermediate values
- reading and following starter code

## Part 1: Reading Starter Code

Students should learn to:
- read the full cell before editing
- identify which line is meant to change
- preserve important variable names
- avoid changing setup code unless asked

Good question:
- What is this code already doing before I touch it?

## Part 2: Lists and Dictionaries in Real Tasks

Challenge notebooks often use:
- lists of values
- dictionaries of settings
- lists of dictionaries
- values pulled from tables or APIs

Students should practice:
- accessing items by index
- accessing dictionary values by key
- looping through records
- printing one item at a time to inspect structure

## Part 3: Functions

Students should be able to:
- define a function
- call a function
- pass inputs
- return results
- test a function with a small example

Example:
```python
def classify_score(score):
    if score > 90:
        return "high"
    elif score > 70:
        return "medium"
    return "low"
```

## Part 4: Small Edits, Fast Checks

A common mistake is making too many changes before testing.

Better approach:
- make one change
- run the cell
- inspect the output
- make the next change

This reduces confusion and helps students find mistakes faster.

## Part 5: Debugging in Notebook Challenges

Helpful habits:
- print variable values
- inspect one record at a time
- read the error message
- check whether earlier cells ran
- compare actual vs expected output

## Part 6: Working With AI While Coding

AI can help explain code and suggest changes, but students should still:
- read the code themselves
- test the result
- understand what changed
- keep the edits small

## Practice Checklist

Students should be able to:
- read starter code without panic
- complete a simple TODO section
- loop through a list of dictionaries
- write and test a function
- inspect a variable with `print()`
- debug a small notebook error
