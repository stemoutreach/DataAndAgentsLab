# pandas and Data Basics

This guide helps students build confidence working with tabular data in Jupyter notebooks.

The focus is on the practical skills that show up often in challenge-style data tasks.

---

## Why This Guide Matters

Students may understand Python but still struggle when they first see a DataFrame.

This guide helps students learn how to:
- load tabular data
- inspect rows and columns
- check for missing values
- select useful columns
- filter data
- summarize what they see

## Part 1: What a DataFrame Is

A DataFrame is a table of data with rows and columns.

Students should understand:
- each row is one record or example
- each column is one field or feature
- values may be numbers, text, dates, or missing data

## Part 2: Core Beginner Commands

Students should become comfortable with:
- `pd.read_csv()`
- `head()`
- `columns`
- `info()`
- `describe()`
- selecting one or more columns
- filtering rows with conditions

Example:

```python
import pandas as pd

df = pd.read_csv("example.csv")
print(df.head())
print(df.columns)
```

## Worked Example: `head()` and `info()`

```python
import pandas as pd

df = pd.DataFrame({
    "machine": ["M-101", "M-102", "M-103"],
    "temperature": [71.2, 89.7, 73.4],
    "status": ["normal", "review", "normal"]
})

print(df.head())
print(df.info())
```

Expected output:

```python
  machine  temperature  status
0   M-101         71.2  normal
1   M-102         89.7  review
2   M-103         73.4  normal
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3 entries, 0 to 2
Data columns (total 3 columns):
...
```

What to notice:
- `head()` shows the first rows
- `info()` shows column counts and types
- together they give a quick first look at the table

## Part 3: Missing Data

Students should learn to ask:
- Are any values missing?
- Which columns have missing data?
- Can missing values be ignored, filled, or flagged?

Common beginner tools:
- `isnull()`
- `sum()`
- `dropna()`
- `fillna()`

### Worked Example: Checking Missing Values

```python
df = pd.DataFrame({
    "temperature": [71.2, None, 73.4],
    "status": ["normal", "review", "normal"]
})

print(df.isnull().sum())
```

Expected output:

```python
temperature    1
status         0
dtype: int64
```

What to notice:
- one temperature value is missing
- this tells you what needs attention before deeper analysis

## Part 4: Filtering and Inspecting

Students should practice:
- keeping only rows that match a condition
- checking unusual values
- sorting to inspect extremes
- comparing subsets of data

### Worked Example: Filtering Rows

```python
review_rows = df[df["status"] == "review"]
print(review_rows)
```

Expected output:

```python
   temperature  status
1          NaN  review
```

What to notice:
- filtering helps you focus on the cases that matter
- filtered rows can still contain missing data

## Part 5: Features and Useful Columns

Students should begin thinking about:
- which columns are useful for the task
- which columns are identifiers only
- which columns may need cleaning first

### Worked Example: Selecting Useful Columns

```python
feature_df = df[["temperature"]]
print(feature_df)
```

Expected output:

```python
   temperature
0         71.2
1          NaN
2         73.4
```

What to notice:
- smaller tables are often easier to inspect
- selecting useful columns helps focus the work

## Part 6: Simple Summaries and Interpretation

Students should be able to explain:
- what the table contains
- which columns matter most
- where missing data appears
- what unusual values stand out
- what they would check next

## Practice Checklist

Students should be able to:
- load a CSV
- inspect rows and columns
- identify numeric vs text columns
- check missing values
- filter rows
- select useful columns
- describe what they see in plain language
