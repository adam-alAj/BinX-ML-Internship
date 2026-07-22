# Day 4: Data Analysis with Pandas

**Date:** Week 1, Day 4  
**Focus:** Mastering tabular data processing using Pandas — DataFrames, data inspection, filtering, missing value handling, grouping, and aggregation.

---

## 📌 Objectives

- Understand core Pandas structures: `Series` and `DataFrame`
- Load and inspect tabular data efficiently
- Perform data selection and conditional filtering (`.loc`, `.iloc`)
- Handle missing data and duplicate records
- Aggregate and group data using `groupby` and `agg`
- Apply all skills to a real-world dataset (MPG automobile dataset)

---

## 📓 Notebook: `Pandas_Data_Analysis.ipynb`

### Section 1: Core Pandas Data Structures

**What was done:**  
Created a `Series` (labeled 1D array) for quarterly revenue and a `DataFrame` from a dictionary containing employee records with intentional missing values.

**Code highlights:**
```python
import pandas as pd
import numpy as np

data_series = pd.Series([100, 200, 300, 400],
                        index=['Q1', 'Q2', 'Q3', 'Q4'],
                        name="Revenue")

raw_data = {
    'Employee_ID': [101, 102, 103, 104, 105, 106, 107],
    'Name': ['Alice', 'Bob', 'Charlie', 'David', 'Eva', 'Frank', 'Grace'],
    'Department': ['HR', 'IT', 'IT', 'Finance', 'HR', 'Finance', 'IT'],
    'Age': [25, 30, 35, np.nan, 22, 40, 29],
    'Salary': [50000, 75000, 82000, 65000, np.nan, 90000, 72000],
    'Experience_Years': [2, 5, 8, 4, 1, 12, np.nan]
}
df = pd.DataFrame(raw_data)
```

**Why it matters:**  
`Series` and `DataFrame` are the fundamental building blocks for all tabular data work in Python — every dataset you load becomes a DataFrame.

---

### Section 2: Data Inspection & Overview

**What was done:**  
Used `.head()`, `.info()`, and `.describe()` to get a quick overview of the dataset's shape, column types, non-null counts, and descriptive statistics.

**Code highlights:**
```python
print(df.head())       # First 5 rows
print(df.info())       # Column types + non-null counts
print(df.describe())   # Summary statistics
```

**Key Findings:**
- 7 employee records, 6 columns
- 3 missing values across `Age`, `Salary`, `Experience_Years`
- Average salary: ~72,333 | Average age: ~30.2 years

**Why it matters:**  
These methods are the standard first step in any Exploratory Data Analysis — they reveal data quality issues, column types, and basic distributions immediately.

---

### Section 3: Data Selection & Boolean Filtering

**What was done:**  
Practiced four essential Pandas selection techniques:
1. **Column selection**: `df[['Name', 'Salary']]`
2. **Boolean masking**: `df[df['Salary'] > 70000]`
3. **`.loc` with multiple conditions**: `df.loc[(Dept == 'IT') & (Salary > 70000), cols]`
4. **`.iloc` integer slicing**: `df.iloc[0:3, 0:4]`

**Code highlights:**
```python
# Boolean mask for high earners
high_earners = df[df['Salary'] > 70000]

# .loc with multiple conditions
it_high_earners = df.loc[(df['Department'] == 'IT') & (df['Salary'] > 70000),
                         ['Name', 'Department', 'Salary']]

# .iloc integer-based slicing
sliced_data = df.iloc[0:3, 0:4]
```

**Why it matters:**  
`.loc` and `.iloc` are the two primary indexing workhorses in Pandas. Boolean filtering is how you answer data questions like "which customers spent more than X?"

---

### Section 4: Data Cleaning & Handling Missing Values

**What was done:**  
Applied three different imputation strategies to handle the missing values:
1. `Age` → filled with **median** age (29.5)
2. `Salary` → filled with **department mean** salary (group-based imputation)
3. `Experience_Years` → filled with **0** (domain-specific default)

**Code highlights:**
```python
# Check missing values
print(df.isnull().sum())

# Impute Age with median
df_clean['Age'] = df_clean['Age'].fillna(df_clean['Age'].median())

# Impute Salary with department mean
df_clean['Salary'] = df_clean.groupby('Department')['Salary']\
                              .transform(lambda x: x.fillna(x.mean()))

# Impute Experience_Years with 0
df_clean['Experience_Years'] = df_clean['Experience_Years'].fillna(0)
```

**Before Cleaning:**
| Column            | Missing |
|-------------------|---------|
| Age               | 1       |
| Salary            | 1       |
| Experience_Years  | 1       |

**After Cleaning:** All missing values filled — 0 remaining.

**Why it matters:**  
Real-world data is almost never clean. Knowing different imputation strategies (median, mean, group-based, domain-specific) is essential for producing reliable ML models.

---

### Section 5: Data Grouping & Aggregation

**What was done:**  
Used `groupby` with the cleaned data to:
1. Calculate **average salary per department**
2. Create a **detailed department summary** with employee count, avg/max salary, and avg experience

**Code highlights:**
```python
avg_salary_per_dept = df_clean.groupby('Department')['Salary'].mean()

dept_summary = df_clean.groupby('Department').agg(
    Employee_count=('Employee_ID', 'count'),
    Avg_salary=('Salary', 'mean'),
    Max_Salary=('Salary', 'max'),
    Avg_Experience=('Experience_Years', 'mean')
).reset_index()
```

**Output:**
| Department | Employee Count | Avg Salary | Max Salary | Avg Experience |
|------------|:--------------:|:----------:|:----------:|:--------------:|
| Finance    | 2              | 77,500     | 90,000     | 8.0            |
| HR         | 2              | 50,000     | 50,000     | 1.5            |
| IT         | 3              | 76,333     | 82,000     | 4.33           |

**Why it matters:**  
Grouped aggregation is how you derive business insights — comparing performance across segments, identifying trends, and generating summary reports.

---

### Section 6: Saving Cleaned Data

**What was done:**  
Saved the fully cleaned DataFrame to `cleaned_employee_data.csv` for downstream use.

```python
df_clean.to_csv('cleaned_employee_data.csv', index=False)
```

**Output file:** [`cleaned_employee_data.csv`](./cleaned_employee_data.csv) — 7 records, 0 missing values.

---

## 🔬 Hands-On Lab: Real Dataset (MPG Automobile Data)

### Step 1: Loading & Inspection
Loaded the **MPG dataset** (398 car models, 9 columns) directly from the official Seaborn GitHub repository.

**Key columns:** `mpg`, `cylinders`, `displacement`, `horsepower`, `weight`, `acceleration`, `model_year`, `origin`, `name`

### Step 2: Missing Value Handling
- Detected 6 missing values in the `horsepower` column
- Imputed using **median** (93.5) — robust against outliers
- 0 duplicate rows found

### Step 3: Filtering & Subset Exploration
Filtered for **high fuel-efficiency cars** (mpg > 30):
- **85 models** out of 398 (21.36%)
- Japanese manufacturers dominated this subset (Toyota Corolla, Datsun, etc.)

### Step 4: Groupby Categorical Aggregation
Grouped by `origin` (manufacturing region) and calculated key metrics:

| Origin  | Avg MPG | Avg HP | Avg Weight | Count |
|---------|:-------:|:------:|:----------:|:-----:|
| Japan   | 30.45   | 79.84  | 2,221      | 79    |
| Europe  | 27.89   | 80.93  | 2,423      | 70    |
| USA     | 20.08   | 118.64 | 3,362      | 249   |

### Final Insights
- **Japan** leads in fuel efficiency (30.45 MPG avg)
- **USA** models prioritize power and size (highest HP and weight → lowest MPG)
- Lighter weight and lower horsepower are strong indicators of high fuel efficiency

---

## ✅ Key Takeaways

- `Series` = 1D labeled array; `DataFrame` = 2D tabular structure with rows & columns
- `.head()`, `.info()`, `.describe()` are the EDA trinity for quick data understanding
- `.loc` (label-based) and `.iloc` (position-based) are the primary indexing methods
- Boolean filtering powers most data selection workflows
- Missing data requires deliberate imputation — one strategy does not fit all
- `groupby` + `agg` enables powerful segmented analysis
- Real-world EDA follows a repeatable pipeline: Load → Inspect → Clean → Filter → Aggregate → Interpret

---

## 🔗 Related Files

- [`Pandas_Data_Analysis.ipynb`](./Pandas_Data_Analysis.ipynb) — Main notebook
- [`cleaned_employee_data.csv`](./cleaned_employee_data.csv) — Cleaned employee dataset output
