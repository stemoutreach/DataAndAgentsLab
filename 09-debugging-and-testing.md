# Debugging and Testing

This guide helps students build one of the most important challenge skills: figuring out what went wrong and checking whether a solution actually works.

With limited prep time, debugging and testing are high-value skills because they support **both** classic AI and agentic AI work in Jupyter notebooks.

---

## Why This Guide Matters

Many students do not get stuck because the task is impossible.

They get stuck because:
- code throws an error
- output looks strange
- a variable is missing
- the notebook was run out of order
- AI-generated code almost works, but not quite
- they do not know what to check next

Good debugging and testing habits help students recover quickly instead of freezing.

## The Main Mindset

Do not ask:
> Why is everything broken?

Ask:
- What exactly failed?
- Where did it fail?
- What did I expect?
- What actually happened?
- What is one small thing I can check next?

## Part 1: Common Kinds of Problems

Students should learn to recognize common categories of problems:

### Syntax Problems
Python cannot read the code structure.

Examples:
- missing colon
- missing parenthesis
- missing quote
- bad indentation

### Name Problems
The code uses something that does not exist yet.

Examples:
- misspelled variable name
- forgot to run an earlier cell
- function name does not match

### Type Problems
The code is using the wrong kind of value.

Examples:
- trying to add text and numbers
- treating a list like a dictionary
- calling a method on the wrong object type

### Logic Problems
The code runs, but the result is wrong.

Examples:
- filtering the wrong column
- passing the wrong argument
- using the wrong threshold
- forgetting an important step

## Part 2: A Simple Debugging Process

A good beginner process is:

1. Read the error message
2. Find the line where the problem happened
3. Look at the nearby code
4. Check whether earlier cells ran
5. Print important values
6. Change one thing at a time
7. Run again and compare results

This works much better than changing many things at once.

## Part 3: Debugging in Jupyter Notebooks

Notebook-specific problems are common.

Students should check:
- Did I run the cells in order?
- Did I rename a variable somewhere?
- Did I change something in an earlier cell?
- Is the notebook state out of sync?
- Should I restart and run the notebook again?

A lot of “mystery” problems come from notebook order, not from advanced coding issues.

## Part 4: Print, Inspect, Compare

One of the simplest debugging tools is `print()`.

Students should use it to:
- inspect variable values
- check list contents
- check dictionary keys
- confirm function inputs
- inspect intermediate results

Helpful questions:
- What value is this variable holding right now?
- Is this what I expected?
- Did this step change the data the way I thought it would?

## Part 5: Testing Small Pieces

Students should test one small part at a time.

Examples:
- test one function with one easy input
- inspect one row instead of the whole table
- test one API response before building a DataFrame
- test one prompt before building a workflow

Small tests make it easier to see what is working and what is not.

## Part 6: Expected vs Actual

A strong debugging habit is comparing:

- expected result
- actual result

Students should get used to saying:
- I expected this column to be numeric, but it is text
- I expected three rows, but I got zero
- I expected a dictionary, but I got a list
- I expected the tool to return a short answer, but it returned a paragraph

That kind of thinking makes debugging much easier.

## Part 7: Testing Edge Cases

Do not only test the “happy path.”

Students should also test:
- missing values
- empty inputs
- extreme values
- weird but possible cases
- incomplete records
- badly formatted output

This matters in both classic AI and agentic AI.

## Part 8: Using AI Well During Debugging

AI can be very helpful for debugging, but students still need to be specific.

Good questions:
- What does this error message mean?
- What type of object is this?
- Why might this filter return zero rows?
- Can you help me debug this one step at a time?
- What should I inspect first?

Weak approach:
- paste everything and ask AI to “fix it”

A better approach is:
- identify the failing part
- ask about that specific part
- test the suggestion
- verify the result

## Part 9: Debugging Agentic Systems

When debugging a prompt or workflow, students should ask:
- Did the prompt say the task clearly?
- Did the output follow the format?
- Was the right context passed forward?
- Did the tool return what the next step needed?
- Did the system make something up?

Sometimes the issue is not the model itself. Sometimes the issue is:
- vague instructions
- bad tool design
- missing context
- weak output requirements

## Part 10: Debugging Data and Model Work

When debugging classic AI or ML tasks, students should ask:
- Did the data load correctly?
- Are the right columns being used?
- Are there missing values?
- Are the feature types what I expected?
- Does the output seem reasonable?
- Are edge cases handled?

A result that looks impressive is not enough. It still needs to make sense.

## Practice Checklist

Students should be able to:
- read an error message without panicking
- find the line where a problem starts
- use `print()` to inspect values
- test one small part at a time
- compare expected vs actual results
- notice when a notebook is out of order
- test edge cases
- ask AI focused debugging questions
- explain what they changed and why

## Final Thought

Debugging is not a sign that you failed.

Debugging is part of solving the problem.

Strong students do not avoid errors. They learn how to work through them carefully.
