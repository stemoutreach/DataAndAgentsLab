# Plotting and Data Visualization

This guide gives students a lightweight introduction to charts and simple visual interpretation for Jupyter notebook work.

The goal is not deep charting skill. The goal is to help students use simple visuals to inspect data and explain what they see.

---

## Why This Guide Matters

Charts help students:
- see patterns faster
- spot unusual values
- compare groups
- understand distributions
- explain results more clearly

Students do not need advanced visualization skills. They only need enough to read and use simple plots with confidence.

## Part 1: What a Plot Helps You See

A plot can help answer questions like:
- Are values spread out or clustered?
- Are there unusual points?
- Do two variables seem related?
- Is one category larger than another?
- Does something change over time?

## Part 2: Common Beginner-Friendly Plots

### Bar Chart
Useful for:
- comparing categories
- showing counts or averages by group

### Line Plot
Useful for:
- showing change over time
- tracking trends

### Histogram
Useful for:
- seeing how numeric values are distributed
- spotting extreme values

### Scatter Plot
Useful for:
- comparing two numeric variables
- spotting clusters or outliers

## Worked Example: Bar Chart

```python
import matplotlib.pyplot as plt

labels = ["day", "night"]
counts = [5, 3]

plt.bar(labels, counts)
plt.xlabel("Shift")
plt.ylabel("Count")
plt.title("Readings by Shift")
plt.show()
```

What to notice:
- bar charts compare categories
- the x-axis shows group names
- the y-axis shows how many are in each group

## Worked Example: Histogram

```python
import matplotlib.pyplot as plt

temps = [71.2, 72.5, 73.1, 89.7, 74.0, 73.8]

plt.hist(temps)
plt.xlabel("Temperature")
plt.ylabel("Frequency")
plt.title("Temperature Distribution")
plt.show()
```

What to notice:
- most values may cluster in one area
- unusual high or low values stand out more clearly
- histograms help show distribution, not categories

## Part 3: Reading a Plot

Students should practice asking:
- What do the axes represent?
- What pattern stands out first?
- Are there unusual points?
- Is one group clearly different?
- Does this support or challenge what I expected?

## Part 4: Beginner Plotting Mindset

Students do not need to make a perfect chart.

They need to:
- choose a simple useful chart
- label it clearly
- use it to inspect the data
- explain what it shows in plain language

## Part 5: Plotting and Classic AI

In classic AI work, plots can help students:
- inspect raw data
- notice missing or unusual patterns
- compare normal vs unusual values
- understand whether results seem reasonable

## Part 6: Plotting and Interpretation

A good student explanation sounds like:
- The histogram shows most values clustered in the middle with a few extreme outliers.
- The scatter plot suggests these two variables move together.
- The bar chart shows one category appears much more often than the others.
- The line plot shows a clear upward trend over time.

## Part 7: Using AI Well With Visualization

AI can help students:
- choose a chart type
- explain what a chart means
- help write plotting code
- help interpret a pattern

Students still need to:
- inspect the actual chart
- check whether the chart matches the task
- explain the meaning in their own words

## Practice Checklist

Students should be able to:
- name four simple plot types
- explain when each is useful
- read axes and basic patterns
- notice outliers or clusters
- describe what a simple chart shows in plain language

## Final Thought

Visualization is not just for presentation.

It is a thinking tool.

A simple chart can help students notice problems, understand data, and make better decisions.
