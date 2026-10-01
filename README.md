# Titanic Data Cleaning

**Task 1 – Data Cleaning and Preprocessing**
Veda Technology | Data Analytics Track | Level 1, Day 1

## About
This project cleans the raw Titanic dataset (891 rows, 12 columns) so it is ready for reliable analysis. I first inspected the data for problems, fixed them step by step, and re-ran the checks to confirm.

## Data quality issues and fixes
| Issue | Fix |
|-------|-----|
| Age: 177 missing values | Filled with median |
| Embarked: 2 missing values | Filled with mode |
| Cabin: 687 missing values (~77%) | Dropped the column |
| Duplicate rows (0 found) | Checked with `duplicated()` |
| Extra spaces / mixed casing in text | `strip()`, `lower()`, `upper()` |
| Wrong data types | Age -> int; Survived, Pclass, Sex, Embarked -> category |
| Fare: 116 outliers | Checked with IQR, kept (real first class fares) |

**Result:** 0 null values and 0 duplicates after cleaning.

## Files
- `titanic_cleaned.csv` – cleaned dataset
- `change_log.csv` – log of every fix
- `Task1_data_cleaning_titanic.ipynb` – full code (Google Colab notebook)
- `Task1_Data_Cleaning_Writeup.pdf` – short write-up of issues and fixes

## Tools used
Python, Pandas, Google Colab

## How to run
1. Open the notebook in Google Colab
2. Load `titanic.csv`
3. Run all cells to get `titanic_cleaned.csv` and `change_log.csv`

## Author
Rabia
