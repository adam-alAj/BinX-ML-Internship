# BinX Tech • AI & Machine Learning Internship Program

Welcome to my repository for the **BinX Tech AI & Machine Learning Internship Program** (Phase 1: Foundations). This repository documents my daily progress, code, labs, and hands-on projects throughout the program.

---

## 👤 About Me

* **Name:** Eng. Adam Alafandi
* **Role:** AI & Machine Learning Intern
* **Location:** Palestine
* **GitHub:** [@adam-alAj](https://github.com/adam-alAj)
* **LinkedIn:** [adam-alafand](https://linkedin.com/in/adam-alafandi)

---

## 🎯 About the Internship

The **BinX Tech AI & ML Internship Program** is an intensive, practical training program designed to build industry-ready skills in Artificial Intelligence, Machine Learning, and Data Science.

* **Track:** Phase 1 — Foundations (40 Hours / Week 1)
* **Focus Areas:** Python Environment Setup, Idiomatic Python, NumPy Numerical Computing, Pandas Data Analysis, and Matplotlib Data Visualization.
* **Core Principle:** Professional, reproducible Jupyter Notebook workflows fully documented with Markdown narratives and pushed regularly via Git/GitHub.

---

## 📅 Internship Daily Progress & Roadmap

```
BinX_ML_Internship/
├── .venv/                            # Shared Virtual Environment
├── week1/             
|     ├── Day_1/                      # Day 1 Lab & Documentation
|     ├── Day_2/                      # Day 2 Lab & Documentation
|     ├── Day_3/                      # Day 3 
|     ├── Day_4/                      # Day 4 (Upcoming)
|     ├── Day_5/                      # Day 5 (Upcoming)
|     .
|     .
|     .                   
├── .gitignore
├── requirements.txt
└── README.md
```

---

### Day 1: Environment Setup & Jupyter Workflow

* **Objective:** Setting up a professional, isolated Python data-science environment and establishing the Jupyter Notebook & Git workflow.
* **Key Tasks & Accomplishments:**
  - Created and activated a Python virtual environment (`.venv`).
  - Installed core libraries: `numpy`, `pandas`, `matplotlib`, and `jupyter`.
  - Configured a clean project folder structure (`BinX_ML_Internship/`).
  - Generated `requirements.txt` and `.gitignore` to ensure repository cleanliness and reproducibility.
  - Developed and tested the first Jupyter Notebook mixing Markdown documentation and executable code.
  - Configured Git and performed initial commits/pushes to GitHub.

---

### Day 2: Python Fundamentals for Data Science & OOP

* **Objective:** Mastering clean, idiomatic Python code, functional programming, list comprehensions, and basic Object-Oriented Programming (OOP).
* **Key Tasks & Accomplishments:**
  - **Data Types & Control Flow:** Utilized primitive data types (`int`, `float`, `str`, `bool`) and composite structures (`list`, `tuple`, `dict`, `set`) along with conditional logic and loops.
  - **Functions & Type Hints:** Authored clean functions with explicit type annotations and standard docstrings for self-documenting code.
  - **List Comprehensions:** Transformed traditional `for` loops into concise, high-performance single-line list comprehensions for data filtering and transformations.
  - **OOP Basics:** Created custom classes (`DataRecord`) encapsulating data attributes and methods for record validation.
  - **Hands-On Drill:** Built a dataset analysis function to compute summary statistics (`mean`, `min`, `max`) on cleaned numerical measurements.
  - **Documentation:** Documented every notebook cell with Markdown explaining **what** the code does and **why** it is used in Data Science / AI workflows.

---

### Day 3: NumPy: Numerical Computing & Vectorized Operations

* **Objective:** Building fluency in multi-dimensional numerical computing using NumPy, leveraging vectorized operations, indexing, boolean masking, and broadcasting instead of slow Python loops.
* **Key Tasks & Accomplishments:**
  - **Array Creation & Inspection:** Created 1D and 2D arrays using multiple initialization methods (`np.array`, `np.zeros`, `np.ones`, `np.arange`, `np.linspace`, `np.random`) and inspected crucial metadata attributes (`shape`, `dtype`, `ndim`).
  - **Multi-Dimensional Slicing & Indexing:** Performed precise array slicing across rows and columns using tuple indexing (`array[row, col]`) to extract specific vectors, sub-matrices, and boundary elements.
  - **Vectorized Operations:** Replaced explicit Python loops with element-wise vectorized arithmetic operations and built-in summary functions (`mean`, `sum`, `std`) for high-performance array computations.
  - **Boolean Masking:** Applied conditional logical expressions directly to matrices to filter, extract, and manipulate specific numeric data points exceeding target statistical thresholds.
  - **Broadcasting Mechanics:** Utilized NumPy broadcasting rules to perform element-wise matrix addition and operations between arrays of compatible but non-matching shapes without unnecessary memory duplication.
  - **Documentation & Reproducibility:** Fixed random seeds (`np.random.seed`) to ensure experimental reproducibility, and thoroughly documented every step in Jupyter Notebook with explanatory Markdown cells.

  ---

### ✅ Day 4: Data Analysis with Pandas

* **Objective:** Mastering tabular data processing — DataFrames, Series, data inspection, filtering, missing value handling, and aggregation.
* **Key Tasks & Accomplishments:**
  - Created **Pandas Series** (labeled 1D arrays) and **DataFrames** from dictionaries.
  - Inspected datasets using `.head()`, `.info()`, and `.describe()` for quick EDA.
  - Performed **column selection**, **boolean masking**, and advanced indexing (`.loc`, `.iloc`).
  - Detected and imputed missing values using **median**, **group mean**, and domain-specific defaults.
  - Aggregated data with **`groupby`** and **`agg`** to compute per-department summary statistics.
  - Saved the cleaned DataFrame to CSV (`cleaned_employee_data.csv`).
  - **Hands-On Lab:** Loaded the real-world **MPG automobile dataset** (398 cars, 9 features) and performed an end-to-end EDA — loading, cleaning, filtering, and grouping by manufacturing region to derive insights on fuel efficiency.
  - **Key Insight:** Japanese cars lead in MPG (avg 30.45) due to lighter weight and lower horsepower compared to US models.

---

### ⏳ Day 5: Data Visualization with Matplotlib & Week 1 Wrap-up *(Upcoming)*

* **Focus:** Plotting line charts, scatter plots, histograms, and bar charts; customizing plot labels, titles, legends; compiling the Week 1 comprehensive report.

---

## 🛠️ Tech Stack & Tools

* **Language:** Python 3.10+
* **Libraries:** NumPy, Pandas, Matplotlib, Jupyter
* **Environment:** VS Code, Windows PowerShell / Command Prompt, Git & GitHub

---

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/adam-alAj/BinX-ML-Internship.git
   cd BinX_ML_Internship
   ```

2. **Activate the virtual environment:**
   ```bash
   .venv\Scripts\activate   # On Windows
   # or
   source .venv/bin/activate # On Linux/Mac
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook:**
   ```bash
   python -m jupyter notebook
   ```

