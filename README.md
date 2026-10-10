# Week 4 Assignment: Statistics, Data Visualization & EDA

This project analyzes the original Week 2 sales dataset and completes the Week 4 assignment requirements in a simple, beginner-friendly way.

## Files included

- `week4_statistics_eda.py` — main project script
- `cleaned_sales_data.csv` — cleaned data used for analysis
- `dataset_before_cleaning.csv` — original raw sales data saved before cleaning
- `dataset_after_cleaning.csv` — cleaned dataset saved after processing
- `dataset_before_cleaning.png` — screenshot of the raw data table
- `dataset_after_cleaning.png` — screenshot of the cleaned data table
- `WEEK4_REPORT.md` — full assignment report with all nine tasks
- `outputs/` — five Matplotlib charts and four Seaborn charts
- `requirements.txt` — Python dependencies

## Original dataset used

The script reads the original raw data from:

../week2_assignment_internnova/sales_data.csv

This is the real Week 2 sales dataset. It is not replaced by the cleaned file.

## Setup

From the project folder, install the dependencies:

```bash
python3 -m pip install -r requirements.txt
```

## Run the project

From the project folder in VS Code, use:

```bash
cd week4_assignment_internnova
python3 week4_statistics_eda.py
```

If you are already inside the project folder, you can run only:

```bash
python3 week4_statistics_eda.py
```

## What the script does

- checks that the raw dataset exists
- inspects the raw data
- records before-and-after cleaning evidence
- cleans missing values and inconsistent text
- calculates statistics and probability
- detects outliers
- creates all required Matplotlib and Seaborn charts
- writes the final report to `WEEK4_REPORT.md`
