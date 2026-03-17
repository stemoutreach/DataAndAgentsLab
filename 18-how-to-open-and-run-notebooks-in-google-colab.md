# 18 How to Open and Run Notebooks in Google Colab

This guide shows students how to open and run the practice notebooks in **Google Colab**.

For most students, Google Colab is the easiest way to use the notebooks because it works in a browser and does not require a local Python setup.

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

Recommended first notebook:
- `notebooks/00-notebook-basics-practice.ipynb`

For the full sequence, see:
- `12-how-to-use-the-practice-notebooks.md`
- `17-four-week-study-plan.md`

---

## Best Student Start Path

1. Find the notebook you want to use in the repository.
2. If the notebook is in **GitHub**, open it from Colab using the GitHub option.
3. If the notebook is in **GitLab**, download the `.ipynb` file and upload it into Colab.
4. Save your own copy if needed.
5. Run the cells from top to bottom.
6. Read the instructions before changing code.

---

## Option 1: Open a Notebook From GitHub

This is usually the easiest option when the notebook is stored in GitHub.

### Steps

1. Open Google Colab.
2. In the file open window, choose the **GitHub** tab.
3. Paste the repo URL or search for the repository.
4. Select the notebook you want to open.
5. Wait for it to load in Colab.
6. Save your own copy if you want to edit your own version.

Why this is useful:
- it lets students open notebooks directly from the repo
- it keeps the notebook source organized
- it is easy for mentors to point students to the right file

---

## Option 2: Open a Notebook From GitLab

If the notebooks are stored in GitLab, the easiest student workflow is usually:

### Steps

1. Open the GitLab repository in your browser.
2. Navigate to the `notebooks/` folder.
3. Select the notebook you want to use.
4. Download the `.ipynb` file.
5. Open Google Colab.
6. In the file open window, choose the **Upload** option.
7. Upload the notebook file.
8. Save your own copy if needed.

### Best student rule

- **GitHub repo** → open from Colab’s GitHub option
- **GitLab repo** → download the notebook, then upload it into Colab

---

## Option 3: Upload a Notebook File Directly

This is useful for pilots or when a notebook is shared directly.

### Steps

1. Open Google Colab.
2. In the file open window, choose the **Upload** option.
3. Select the `.ipynb` file from your computer.
4. Wait for it to load.
5. Run the notebook cells in order.

This is simple, but students also need the data files if the notebook uses CSVs.

---

## Option 4: Open From Google Drive

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

If the notebook opens from GitHub, GitLab, or another shared source:
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
2. Confirm that the data file is available along with the notebook.
3. Re-run the setup cell near the top of the notebook.
4. Print the data path being used.
5. Ask your mentor whether you should:
   - upload the CSV manually
   - use a different folder location
   - reopen the notebook from the repository

A file path problem does not usually mean your code is wrong.
It often means the notebook cannot see the data file yet.

---

## Best Workflow for Students Using GitLab

If your class or team stores notebooks in GitLab, this is the simplest workflow:

1. Open GitLab
2. Download the notebook file
3. Open Colab
4. Upload the notebook
5. Upload the matching CSV if the notebook needs one
6. Save your own copy
7. Start at the top and run the cells in order

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

## Final Reminder

For most students, Google Colab is the best default way to run these notebooks.

After you open the notebook:
- start with notebook 00
- follow the study plan
- use AI as a helper
- keep going one step at a time
