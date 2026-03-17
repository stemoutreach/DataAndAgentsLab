# Classic AI Training Guide

This guide prepares students for challenge-style work that involves data, tabular analysis, simple machine learning workflows, anomaly detection, and result interpretation in **Jupyter notebooks**.

The focus is not on deep math. The focus is on learning how to work carefully with data, models, and results.

---

## Learning Goals

By the end of this guide, students should be able to:
- load and inspect tabular data
- use pandas for beginner-friendly analysis
- identify useful features
- understand train, validation, and test concepts
- explain why scaling or preprocessing may be needed
- understand the basic idea of anomaly detection
- test outputs and edge cases
- add simple rule-based guardrails
- explain results in plain language
- use AI to support the workflow without blindly trusting it

## Core Skills Needed First

Before starting this path, students should be comfortable with:
- Jupyter notebook basics
- Python variables, lists, dictionaries, loops, and functions
- basic debugging
- rows, columns, and simple tables

Helpful support guide:
- [07 pandas and Data Basics](./07-pandas-and-data-basics.md)

## Part 1: Data Exploration

Students should practice:
- loading a CSV into pandas
- checking the first few rows
- reading column names
- identifying numeric vs text columns
- checking for missing values
- noticing strange or extreme values

Questions to ask:
- What does each row represent?
- What does each column mean?
- Which columns seem useful?
- Is anything missing or suspicious?

### Worked Example: Exploring a Small Dataset

```python
import pandas as pd

df = pd.DataFrame({
    "temperature": [71.2, 89.7, 73.4],
    "vibration": [0.12, 1.05, 0.18],
    "status": ["normal", "review", "normal"]
})

print(df.head())
print(df.columns)
```

Expected output:

```python
   temperature  vibration  status
0         71.2       0.12  normal
1         89.7       1.05  review
2         73.4       0.18  normal
Index(['temperature', 'vibration', 'status'], dtype='object')
```

What to notice:
- the second row looks unusual
- `temperature` and `vibration` are likely useful features
- `status` looks like an outcome or label

## Part 2: Beginner pandas Skills

Students should become comfortable with:
- `read_csv()`
- `head()`
- `info()`
- `describe()`
- selecting columns
- filtering rows
- checking null values
- creating smaller working tables

Students do not need to memorize every command, but they should be able to read and use them.

## Part 3: Features and Model Inputs

Students should understand:
- a feature is a piece of information the model can use
- some columns may be useful and others may not
- poor feature choices can hurt results
- data often needs cleanup before modeling

Good beginner questions:
- Which columns help describe the problem?
- Which columns are identifiers only?
- Are there text fields that need special handling?
- Are some values missing or inconsistent?

### Worked Example: Choosing Useful Columns

```python
feature_df = df[["temperature", "vibration"]]
print(feature_df)
```

Expected output:

```python
   temperature  vibration
0         71.2       0.12
1         89.7       1.05
2         73.4       0.18
```

What to notice:
- this smaller table keeps only the fields likely useful for simple detection
- removing unnecessary columns can make later work easier

## Part 4: Train, Validation, and Test Thinking

Students do not need advanced statistics, but they should understand the idea:

- training data helps build the model
- validation data helps compare choices
- test data helps check final performance

This helps students avoid the mistake of judging a model only on the same data it already saw.

## Part 5: Scaling and Preprocessing

Students should know that models often work better when data is prepared carefully.

Examples include:
- handling missing values
- selecting the right columns
- scaling numeric features
- removing clearly unusable data

Students should understand the reason, even if helper code is provided.

## Part 6: Anomaly Detection Intuition

Students should understand anomaly detection in simple terms:

An anomaly is something unusual compared with the normal pattern.

This is useful when:
- labeled examples are limited
- the goal is to find unusual behavior
- you want to flag possible issues for review

Students should be able to ask:
- Does this result seem reasonable?
- Are too many items being flagged?
- Are obvious strange cases being caught?
- Does the model miss things a human would expect to notice?

## Part 7: Testing and Edge Cases

Students should test:
- normal-looking examples
- clearly unusual examples
- missing or incomplete inputs
- extreme values
- weird combinations of values

This is important because a model that looks fine on one example may fail on another.

## Part 8: Guardrails and Rule-Based Checks

Students should learn that a model does not have to work alone.

Sometimes a better solution is:
- model output
- plus a few human-written rules
- plus simple validation checks

Example ideas:
- reject impossible values
- flag incomplete rows
- add threshold checks
- require manual review for risky cases

### Worked Example: Simple Guardrail

```python
def needs_review(temp, vibration):
    return temp >= 85 or vibration >= 0.90

print(needs_review(72, 0.12))
print(needs_review(90, 0.20))
print(needs_review(70, 1.05))
```

Expected output:

```python
False
True
True
```

What to notice:
- this is a simple rule, not a full model
- even simple checks can help catch suspicious cases
- guardrails are useful when stakes matter

## Part 9: Interpreting and Reporting Results

Students should be able to explain:
- what data they used
- what approach they tried
- what the output means
- where the model seems strong
- where it may fail
- what they would improve next

A good result is not only code that runs. A good result is a solution the student can explain.

## Part 10: Using AI Well in Classic AI Work

Good uses of AI:
- explain pandas code
- explain an error
- suggest how to inspect missing data
- help compare feature choices
- help write a short result summary

Weak uses of AI:
- asking for a full answer without understanding the data
- trusting a model interpretation without checking outputs
- submitting code the student cannot explain

## Practice Checklist

Students should be able to:
- load and inspect a dataset
- identify useful columns
- explain missing values
- describe what a feature is
- explain train vs test in simple language
- explain what anomaly detection means
- test a few edge cases
- add a simple rule-based check
- describe results in plain English
