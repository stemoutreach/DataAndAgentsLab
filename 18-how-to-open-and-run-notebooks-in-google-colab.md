# 18 How to Open and Run Notebooks in Google Colab

For most students, **Google Colab** is the easiest way to run these notebooks because it works in a browser and does not require a local Python setup.

## Start Here

1. Open [Google Colab](https://colab.research.google.com/).
2. Get the notebook you want to use from the repository.
3. Open it in Colab.
4. Save your own copy if needed.
5. Run the cells from top to bottom.

Recommended first notebook:
- `notebooks/00-notebook-basics-practice.ipynb`

For the full notebook sequence, see:
- `12-how-to-use-the-practice-notebooks.md`
- `17-four-week-study-plan.md`

## How to Open the Notebook

### If the notebook is in GitHub
1. Open Colab.
2. Choose the **GitHub** option.
3. Find the notebook.
4. Open it.

### If the notebook is in GitLab
1. Open GitLab.
2. Go to the `notebooks/` folder.
3. Download the `.ipynb` file.
4. Open Colab.
5. Use the **Upload** option to upload the notebook.

### Best student rule
- **GitHub repo** → open from Colab’s GitHub option
- **GitLab repo** → download the notebook, then upload it into Colab

## How to Work in Colab

- start at the top
- read the instructions first
- run one cell at a time
- check the output after each step
- make small changes
- save your work

## Data File Note

Some notebooks use CSV files from the repo’s `data/` folder.

Examples:
- `data/practice_sensor_data.csv`
- `data/practice_sensor_data_large.csv`
- `data/practice_equipment_data.csv`

If a notebook gives a `FileNotFoundError`:
1. check whether the notebook uses a CSV
2. make sure the matching data file is available
3. rerun the setup cell near the top
4. ask your mentor if you also need to upload the CSV

## If You Get Stuck

- rerun earlier cells
- read the error message
- check whether the data file is available
- ask one focused AI question
- ask a mentor after you have tried

## Final Reminder

For most students, **Google Colab is the default way to run these notebooks**.

Start with notebook 00, follow the study plan, and work one step at a time.
