# 18 How to Open and Run Notebooks in Google Colab

This guide shows students how to open and run the practice notebooks in **Google Colab**.

Google Colab is a browser-based notebook environment. Google describes Colab as a hosted Jupyter notebook service that requires no setup and provides a student-friendly browser interface.

For most students, this is the easiest way to use the notebooks.

---

## When to Use Google Colab

Use Google Colab if:
- you are working on a school or personal laptop without Python installed
- you want to use the notebooks in a browser
- you want the easiest path to get started

Use local Jupyter only if:
- you already have Python and Jupyter working on your computer
- your mentor told you to use a local setup

---

## Before You Start

You will need:
- a Google account
- access to the notebook files
- access to the repo data files if the notebook uses a CSV

Helpful starting point:
- Google Colab home: https://colab.research.google.com/
- Google Colab intro notebook: https://colab.research.google.com/notebooks/intro.ipynb

---

## Best Student Start Path

1. Open Google Colab
2. Open the notebook you want to use
3. Save your own copy if needed
4. Run the cells from top to bottom
5. Read the instructions before changing code

Recommended first notebook:
- `notebooks/00-notebook-basics-practice.ipynb`

For the full sequence, see:
- `12-how-to-use-the-practice-notebooks.md`
- `17-four-week-study-plan.md`

---

## Option 1: Open a Notebook From GitHub

This is usually the best option once the repo is published.

### Steps

1. Go to Google Colab.
2. In the file open window, choose the **GitHub** tab.
3. Paste the repo URL or search for the repository.
4. Select the notebook you want to open.
5. Wait for it to load in Colab.
6. Save a copy if you want to edit your own version.

Why this is useful:
- it lets students open notebooks directly from the repo
- it keeps the notebook source organized
- it is easy for mentors to point students to the right file

---

## Option 2: Upload a Notebook File

This is useful for pilots or when a notebook is shared directly.

### Steps

1. Go to Google Colab.
2. In the file open window, choose the **Upload** option.
3. Select the `.ipynb` file from your computer.
4. Wait for it to load.
5. Run the notebook cells in order.

This is simple, but students also need the data files if the notebook uses CSVs.

---

## Option 3: Open From Google Drive

This works well if notebooks are shared through Drive.

### Steps

1. Put the notebook file into Google Drive.
2. Open Google Colab.
3. Choose the **Google Drive** tab.
4. Select the notebook.
5. Open it and save your own copy if needed.

This is useful if a class or mentor shares materials through Drive.

---

## How to Run the Notebook

Once the notebook is open:

1. Start at the top.
2. Read the markdown instructions first.
3. Run one code cell at a time.
4. Check the output after each step.
5. Make small changes instead of many changes at once.
6. If something breaks, read the error message and inspect the previous cells.

Remember:
- notebook cells often depend on earlier cells
- if you run cells out of order, the notebook may fail
- restarting and rerunning can often fix notebook state problems

---

## How to Save Your Work

A good habit is to save your own working copy.

If the notebook opens from GitHub or another shared source:
- save a copy into your own Google Drive before doing a lot of work

That way:
- you do not overwrite shared files
- your work is easier to find later
- you can return to your progress

---

## How Data Files Work

Some notebooks use CSV files from the repo’s `data/` folder.

Examples:
- `data/practice_sensor_data.csv`
- `data/practice_sensor_data_large.csv`
- `data/practice_equipment_data.csv`

Several notebooks in this repo include a small setup cell that checks common file paths automatically, such as:
- `data/...`
- `../data/...`

That helps, but students may still need to make sure the data file is available in Colab.

---

## What to Do If a Data File Does Not Load

If you get a `FileNotFoundError`, try these steps:

1. Check whether the notebook uses a CSV file.
2. Confirm that the data file was uploaded or is available in the same repo structure.
3. Re-run the setup cell near the top of the notebook.
4. Print the data path being used.
5. Ask your mentor whether you should:
   - upload the CSV manually
   - open the notebook from GitHub instead
   - use a different folder location

A file path problem does not usually mean your code is wrong.
It often means the notebook cannot see the data file yet.

---

## Good Student Habits in Colab

- run cells from top to bottom
- read the instructions before editing code
- save your own copy
- check outputs after each step
- ask small AI questions if stuck
- keep notes on what worked and what did not

---

## Common Problems

### Problem: I ran a later cell first
Fix:
- go back and run the earlier cells in order

### Problem: The notebook says a variable does not exist
Fix:
- check whether you skipped a setup cell
- restart and rerun from the top if needed

### Problem: The CSV file cannot be found
Fix:
- check the data file location
- rerun the setup cell
- upload the file if needed

### Problem: I changed too much and now I am lost
Fix:
- undo the last few edits if possible
- compare to the original notebook
- make one smaller change next time

---

## Best Advice for Students

Use Colab as your workspace, not as the place where all your thinking happens.

The important part is still:
- reading the task
- testing your code
- checking outputs
- using AI carefully
- learning from mistakes

Colab makes the notebooks easier to open.
It does not replace problem solving.

---

## Final Reminder

For most students, **Google Colab is the best default way to run these notebooks** because it is browser-based and easy to start with. Official Colab pages emphasize that it is a hosted Jupyter notebook service with zero setup and a student-friendly browser interface. citeturn640187search0

After you open the notebook:
- start with notebook 00
- follow the study plan
- use AI as a helper
- keep going one step at a time
