# APIs, JSON, and Live Data

This guide helps students understand how challenge notebooks may use live or external data.

The focus is on beginner-friendly API and JSON skills that students can use in Jupyter notebooks.

---

## Why This Guide Matters

Some notebook tasks do not start with a clean CSV file. Instead, the data may come from an API.

Students should understand:
- what an API is
- what JSON looks like
- how to request data
- how to inspect the response
- how to turn the result into a usable table

## Part 1: What an API Is

An API is a way for one program to request information from another system.

A notebook may use an API to get:
- weather data
- sensor data
- public datasets
- current values from a service

## Part 2: What JSON Is

JSON is a common format for structured data.

It often looks like:
- dictionaries
- lists
- nested dictionaries and lists

Students should practice:
- reading keys and values
- noticing nested structure
- printing one small part at a time

### Worked Example: Nested JSON

```python
sample_data = {
    "site": "Plant-7",
    "readings": [
        {"machine": "M-101", "temperature": 71.2, "meta": {"shift": "day", "zone": "A"}},
        {"machine": "M-102", "temperature": 89.7, "meta": {"shift": "night", "zone": "B"}}
    ]
}

print(sample_data["site"])
print(sample_data["readings"][1]["machine"])
print(sample_data["readings"][1]["meta"]["zone"])
```

Expected output:

```python
Plant-7
M-102
B
```

What to notice:
- JSON can be nested several levels deep
- inspecting one small part at a time makes it easier to understand

## Part 3: Requesting Data

Students should understand the basic idea of:
- sending a request
- getting a response
- checking whether the response worked
- converting the result into Python data

Example:

```python
import requests

response = requests.get("https://example.com/data")
print(response.status_code)
data = response.json()
```

## Part 4: Inspecting the Response

Before doing anything complicated, students should inspect:
- the response status
- the top-level structure
- the available keys
- one sample record

Helpful habits:
- print the keys
- print one item
- avoid trying to understand the whole response at once

### Worked Example: Build a Smaller Table

```python
records = []
for reading in sample_data["readings"]:
    records.append({
        "machine": reading["machine"],
        "temperature": reading["temperature"],
        "zone": reading["meta"]["zone"]
    })

print(records)
```

Expected output:

```python
[{'machine': 'M-101', 'temperature': 71.2, 'zone': 'A'},
 {'machine': 'M-102', 'temperature': 89.7, 'zone': 'B'}]
```

What to notice:
- not all JSON is already table-shaped
- sometimes you need to build a smaller structure that keeps only the useful fields

## Part 5: Turning JSON Into a Table

Sometimes the goal is to turn JSON into a DataFrame.

Students should understand that:
- not all JSON is already table-shaped
- nested data may need cleanup
- some fields may be missing
- it is okay to build a smaller table with only the needed fields

## Part 6: Error Handling and Real-World Messiness

Students should expect:
- missing fields
- failed requests
- extra nested structure
- inconsistent values

Good questions:
- Did the request work?
- Is the data shaped the way I expected?
- Which fields do I actually need?
- What should I do if something is missing?

## Part 7: Using AI Well With API Work

AI can help students:
- explain JSON structure
- suggest how to inspect nested data
- explain an error
- help map fields into a smaller table

Students should still:
- inspect the actual response
- test code in small steps
- check whether the fields match the task

## Practice Checklist

Students should be able to:
- explain what an API is
- explain what JSON is
- inspect a response status
- read keys from a JSON object
- inspect one record at a time
- describe how JSON could become a table
