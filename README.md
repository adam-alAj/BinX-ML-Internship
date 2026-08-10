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

* **Track:** Phase 1 — Foundations (40+ Hours) → Phase 2 — Statistical Analysis & ML Foundations → Evaluation, Tuning & Pipelines (In Progress)
* **Focus Areas:** Python Environment Setup, Idiomatic Python, NumPy Numerical Computing, Pandas Data Analysis, Matplotlib Data Visualization, Statistical Analysis with Real Datasets, and scikit-learn Machine Learning Workflows.
* **Core Principle:** Professional, reproducible Jupyter Notebook workflows fully documented with Markdown narratives and pushed regularly via Git/GitHub.

---

## 📅 Internship Daily Progress & Roadmap

```
BinX_ML_Internship/
├── .venv/                             # Shared Virtual Environment
├── BinX_Week_01/                      # Week 1: Foundations (Completed ✅)
│   ├── Day1/                          # Environment Setup
│   ├── Day2/                          # Python Fundamentals & OOP
│   ├── Day3/                          # NumPy Numerical Computing
│   ├── Day4/                          # Pandas Data Analysis
│   └── Day5/                          # Data Visualization Mini-Project
├── BinX_Week_02/                      # Week 2: Statistics & ML (Completed ✅)
│   ├── Day1/                          # Descriptive Statistics on Real Dataset
│   ├── Day2/                          # Probability Fundamentals & Distributions
│   ├── Day3/                          # Vectors, Matrices & Predictions (Linear Algebra for ML)
│   ├── Day4/                          # Univariate EDA on a Real Dataset
│   └── Day5/                          # Comprehensive EDA Full Pipeline
├── BinX_Week_03/                      # Week 3: ML Workflow Foundations (Completed ✅)
│   ├── Day1/                          # Setting Up the ML Workflow
│   ├── Day2/                          # Linear Regression Predictions
│   ├── Day3/                          # Logistic Regression Classifier
│   ├── Day4/                          # Model Comparison & Feature Importance
│   └── Day5-mini-project/             # End-to-End Titanic Survival Prediction
├── BinX_Week_04/                      # Week 4: Evaluation, Tuning & Pipelines (In Progress)
│   ├── Day1/                          # Three-Way Split (Train / Validation / Test)
│   └── Day2/                          # Cross-Validating a Model (5-Fold CV)
├── .gitignore
├── requirements.txt
└── README.md                          # ← You are here
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

### ✅ Day 5: Data Visualization Mini-Project & EDA

* **Objective:** Integrating all Week 1 skills (NumPy, Pandas, Matplotlib) into a comprehensive exploratory data analysis with visual communication.
* **Key Tasks & Accomplishments:**
  - Loaded the **MPG automobile dataset** (398 cars, 9 features) from the Seaborn GitHub repository.
  - Engineered new features using **vectorized NumPy operations**: converted MPG to KPL (Kilometers Per Liter) and created an `efficiency_category` column (High/Medium/Low).
  - Computed **NumPy statistical metrics** (mean, std dev, percentiles, IQR) on weight and horsepower arrays.
  - **Line Plot:** Tracked average MPG over model years (1970–1982), revealing a ~76% efficiency increase driven by oil crises and CAFE standards.
  - **Scatter Plot:** Visualized the strong negative correlation between vehicle weight and MPG, colored by manufacturing origin (USA, Europe, Japan).
  - **Bar Plot:** Compared average MPG by origin — Japan leads (30.45 MPG), USA lags (20.08 MPG).
  - **Histogram:** Identified a bimodal MPG distribution reflecting two distinct market segments (economy vs. performance).
  - **Combined 2×2 Subplots Grid:** Merged all four visualizations into a professional, publication-ready figure.
  - **Key Insight:** Weight is the strongest predictor of fuel economy; Japanese cars dominate efficiency due to lighter design and lower horsepower.

---

## 📅 Week 2: Statistical Analysis & Machine Learning Foundations (Completed ✅)

---

### ✅ Day 1: Descriptive Statistics on a Real Dataset

* **Objective:** Computing and interpreting descriptive statistics (central tendency & dispersion) on a real-world dataset.
* **Dataset:** Titanic passenger list (891 records) — analyzed the `Fare` column.
* **Key Tasks & Accomplishments:**
  - Loaded the Titanic dataset from a public GitHub repository using Pandas (`pd.read_csv`).
  - Calculated **central tendency** metrics:
    - **Mean:** \$32.20 (inflated by luxury-class outliers)
    - **Median:** \$14.45 (better represents the typical passenger)
    - **Mode:** \$8.05 (most common fare paid)
  - Calculated **dispersion/spread** metrics:
    - **Variance:** 2469.44
    - **Standard Deviation:** \$49.69 (high variability)
    - **IQR:** \$23.09 (middle 50% range: \$7.91 – \$31.00)
  - Detected **right-skewness** by comparing Mean (\$32.20) vs Median (\$14.45) — the mean is pulled upward by extreme high-value fares (up to \$512.33).
  - Concluded that the **Median is the preferred measure** of center for skewed data, as over 70% of passengers paid less than the mean price.
  - Wrote a **plain-language summary report** bridging raw statistics to actionable insights.
  - **Tools used:** NumPy (`np.mean`, `np.median`, `np.percentile`, `np.var`, `np.std`), Pandas (`pd.read_csv`, `.dropna()`), SciPy (`stats.mode`).

### ✅ Day 2: Probability Fundamentals & Probability Distributions

* **Objective:** Understanding core probability concepts and common probability distributions through Python numerical simulations.
* **Key Tasks & Accomplishments:**
  - Simulated **fair coin flips** at increasing trial sizes (10 to 100,000) to demonstrate the **Law of Large Numbers** — empirical probability converged to 0.5.
  - Applied **Conditional Probability & Bayes' Theorem** on synthetic email data to simulate a spam filter scenario.
  - Visualized and analyzed **four key probability distributions**:
    - **Normal Distribution:** Simulated human heights (mean=170cm, std=10cm) — bell curve.
    - **Binomial Distribution:** Coin flip success counts with `scipy.stats.binom`.
    - **Poisson Distribution:** Modeled customer arrival rates ($\lambda = 5$).
    - **Uniform Distribution:** Continuous random sampling over $[0, 1)$.
  - Verified the **Empirical Rule (68-95-99.7)** for the Normal Distribution.
  - Connected each distribution to its real-world **Machine Learning application**.
  - **Tools used:** NumPy (`np.random`), SciPy (`stats.norm`, `stats.binom`, `stats.poisson`, `stats.uniform`), Matplotlib, Seaborn.

### ✅ Day 3: Vectors, Matrices & Predictions — Linear Algebra Foundations for ML

* **Objective:** Mastering linear algebra concepts in NumPy and connecting them to how ML models represent data and make predictions.
* **Key Tasks & Accomplishments:**
  - **Vectors & Dot Products:** Created feature vectors (house area, bedrooms, age) and weight vectors, computing dot products via manual loops, `np.dot()`, and the `@` operator. Calculated L2 norms with `np.linalg.norm()`.
  - **Matrices & Transpose:** Built a dataset matrix $X$ with 5 samples × 3 features, and explored transposition with `.T`.
  - **Batch Predictions:** Used matrix-matrix multiplication $(X \cdot W)$ to compute two outputs (Price & Rent) simultaneously across all samples, verifying the $(m \times n) \times (n \times p) \to (m \times p)$ shape rule.
  - **Linear Regression Simulation:** Generated random synthetic data (10 samples, 4 features) and computed predictions $\hat{y} = Xw + b$ using `np.dot()` with a bias term.
  - **Shape Error Handling:** Deliberately triggered and caught a `ValueError` for dimension mismatch, then corrected the weight matrix shape to resolve it.
  - **Tools used:** NumPy (`np.dot`, `np.matmul`, `@`, `np.linalg.norm`, `np.random`, `.shape`, `.T`).

### ✅ Day 4: Univariate EDA on a Real Dataset

* **Objective:** Conducting a comprehensive univariate exploratory data analysis on a real-world dataset using Seaborn and Pandas.
* **Dataset:** Titanic passenger dataset (891 records, 15 columns) loaded via `sns.load_dataset("titanic")`.
* **Key Tasks & Accomplishments:**
  - **Histograms + KDE:** Plotted distributions for `age`, `fare`, `sibsp`, `parch` — found `age` roughly normal, `fare` heavily right-skewed, `sibsp`/`parch` discrete and skewed toward 0.
  - **Box Plots:** Visualized outliers in `age` (infants & elderly) and `fare` (extreme right-side outliers up to $500).
  - **IQR Outlier Detection:** Applied the IQR method to `fare` — flagged 116 outliers (~13%). Decided to **cap (winsorize)** rather than drop to retain valid 1st-class luxury ticket data.
  - **Count Plots:** Visualized categorical variables (`sex`, `class`, `embarked`, `survived`) with percentage annotations — documented mild-to-significant class imbalances (e.g., target 61.6%/38.4%).
  - **Summary:** Documented modeling implications: log-transformation for skewed features, F1-Score for imbalanced target, encoding strategy for categoricals.
  - **Tools used:** Pandas, NumPy (`np.where` for capping), Matplotlib, Seaborn (`histplot`, `boxplot`, `countplot`).

### ✅ Day 5: Comprehensive EDA — Full Pipeline

* **Objective:** Combining descriptive statistics, univariate/bivariate analysis, outlier detection, correlation analysis, and data storytelling into a single reproducible ML-ready pipeline.
* **Dataset:** Titanic passenger dataset (891 records, 12 columns) loaded from raw GitHub source.
* **Key Tasks & Accomplishments:**
  - **Summary Statistics:** Computed `.describe()` on all numeric columns — 38.4% survival rate, mean age 29.7, fare heavily right-skewed.
  - **Missing Value Analysis:** Found Age (19.9%), Cabin (77.1%), and Embarked (0.2%) missing — documented handling strategies for each.
  - **Univariate Analysis:** Histograms + KDE for numeric variables; count plots for categorical variables with percentage annotations.
  - **Outlier Detection:** Box plots and IQR method on `fare` — flagged 116 outliers (~13%), capped at upper bound.
  - **Bivariate Analysis:** Explored relationships between every feature and `Survived` — sex (females ~74% survival), class (1st class ~63%), and fare were strongest predictors.
  - **Correlation Analysis:** Computed Pearson correlation matrix + heatmap — key correlations: Survived↔Sex (0.54), Survived↔Pclass (-0.34), Pclass↔Fare (-0.55).
  - **Data Storytelling:** Compiled all insights into ML recommendations — feature engineering (FamilySize, Age bins, Title extraction), encoding strategy (OHE, Ordinal), algorithm selection (Gradient Boosting / Random Forest), and evaluation (F1-Score, ROC-AUC).
  - **Tools used:** Pandas, NumPy, Matplotlib, Seaborn (`histplot`, `boxplot`, `countplot`, `barplot`, `heatmap`), IQR method, Pearson correlation.

---

### 📅 Week 3: Machine Learning Workflow Foundations (Completed ✅)

#### ✅ Day 1: Setting Up the ML Workflow
* **Objective:** Establishing a clean and reproducible machine learning workflow using a notebook-first structure.
* **Key Tasks & Accomplishments:**
  - Organized the notebook workflow around a practical data-to-model progression.
  - Loaded and inspected the dataset to understand its general shape and columns.
  - Separated the target variable from the feature space in preparation for modeling.
  - Documented the baseline workflow for future experimentation and reuse.

#### ✅ Day 2: Predicting Continuous Values with Linear Regression
* **Objective:** Implementing a complete Linear Regression workflow to predict continuous values, interpret coefficients, and validate model performance against a baseline.
* **Key Tasks & Accomplishments:**
  - Loaded the California Housing dataset and selected a 5-feature subset for modeling.
  - Trained a `LinearRegression` model and extracted intercept/coefficients to interpret feature influence.
  - Evaluated model performance on unseen test data using **MAE** (~0.58), **RMSE** (~0.80), and **R²** (~0.51).
  - Constructed a naive mean-baseline predictor and compared its RMSE (~1.14) against the model RMSE.
  - Verified the model delivers a **~30% error reduction** over the baseline, confirming predictive value.
  - Documented coefficient interpretation and business insights in reproducible Markdown.
* **Tools used:** `scikit-learn` (`LinearRegression`, `train_test_split`, metrics), NumPy, Pandas, Matplotlib, Seaborn.

#### ✅ Day 3: Building and Evaluating a Logistic Regression Classifier
* **Objective:** Implementing a complete binary classification workflow to predict customer churn — training a Logistic Regression model, evaluating it with a Confusion Matrix, interpreting Precision/Recall/F1 metrics, and assessing discrimination power using the ROC curve and AUC.
* **Key Tasks & Accomplishments:**
  - Generated a synthetic customer churn dataset (1,000 samples, 5 features, ~25% churn) using `make_classification` and performed a stratified 80/20 train/test split.
  - Trained a `LogisticRegression` model and interpreted the intercept (-0.5307) and coefficients: `Contract_Length` (+0.4619) and `Payment_Delay` (+0.2257) raise churn odds, `Support_Calls` (-0.2958) lowers them.
  - Evaluated predictions on the test set with a **Confusion Matrix** (TN=142, FP=7, FN=38, TP=13).
  - Computed Churn-class metrics: **Precision 0.6500**, **Recall 0.2549**, **F1-Score 0.3662**, overall accuracy 78%.
  - Concluded **Recall is the priority metric** for churn: a missed churner (FN) costs customer lifetime value, while a False Positive only costs a low-value retention offer.
  - Assessed discrimination capability with the **ROC-AUC score (0.6986)** and ROC curve vs. random chance — moderate performance.
  - Documented next steps: feature engineering, threshold tuning, and non-linear models (Random Forest, XGBoost) to improve recall.
* **Tools used:** `scikit-learn` (`make_classification`, `LogisticRegression`, `train_test_split`, `confusion_matrix`, `classification_report`, `roc_auc_score`, `roc_curve`), NumPy, Pandas, Matplotlib, Seaborn.

#### ✅ Day 4: Model Comparison & Feature Importance
* **Objective:** Performing a comprehensive model selection study by benchmarking four classification algorithms — Decision Tree, Random Forest, SVM, and k-NN — on a customer churn dataset, and justifying the winning model with metrics and theory.
* **Key Tasks & Accomplishments:**
  - Generated a synthetic churn dataset (1,000 samples, 8 features, 80% stay / 20% churn) consistent with Day 3, and performed a stratified 80/20 split with `StandardScaler` fit on train only.
  - Trained four classifiers: **Decision Tree** (`max_depth=5`), **Random Forest** (100 trees), **SVM (RBF kernel)**, and **k-NN (k=5)**.
  - Compared all models using **Accuracy, Precision, Recall, F1-Score, and AUC-ROC** — **k-NN (k=5) won with F1-Score 0.8000, Accuracy 93.0%, and perfect Precision 1.0000** (zero false positives).
  - Analyzed Random Forest **feature importances** — `monthly_charges` (0.280) and `tenure_months` (0.232) are the strongest churn drivers.
  - Justified the winning model from both empirical metrics and theoretical characteristics (scaling benefit, tight local clusters, tree split limitations).
* **Tools used:** `scikit-learn` (`DecisionTreeClassifier`, `RandomForestClassifier`, `SVC`, `KNeighborsClassifier`, `StandardScaler`, `train_test_split`, metrics), NumPy, Pandas, Matplotlib, Seaborn.

#### ✅ Day 5: End-to-End Titanic Survival Prediction Mini-Project
* **Objective:** Building a complete end-to-end Machine Learning pipeline — from raw data to a selected model — that predicts passenger survival on the Titanic dataset, tying together workflow design, preprocessing, baseline benchmarking, classification, evaluation, and model selection.
* **Key Tasks & Accomplishments:**
  - Loaded the **Titanic dataset** (891 passengers) from Seaborn, selected 7 features, and split **80/20 with stratification before any preprocessing** to prevent data leakage.
  - Built a `ColumnTransformer` pipeline — median imputation + `StandardScaler` for numeric features, most-frequent imputation + `OneHotEncoder(drop='first')` for categoricals — fitted **on the training set only**.
  - Established a **DummyClassifier baseline** (most-frequent class): 61.5% accuracy, 0.0 Precision/Recall/F1, AUC 0.5.
  - Trained **Logistic Regression** (79.9% accuracy, Precision 77.9%, Recall 66.7%, F1 0.72, AUC 0.84) and **Random Forest** (81.0% accuracy, Precision 85.7%, Recall 60.9%, F1 0.71, AUC 0.84).
  - Broke down the **Confusion Matrices** — Logistic Regression: TN=97, FP=13, FN=23, TP=46; Random Forest: TN=103, FP=7, FN=27, TP=42 — and visualized them with a heatmap plus a full performance comparison bar chart.
  - **Selected Random Forest** as the winning model: highest Precision (85.7%) and Accuracy (81.0%), comparable AUC-ROC, and natural capture of non-linear interactions ("women and children first").
* **Tools used:** `scikit-learn` (`train_test_split`, `ColumnTransformer`, `Pipeline`, `SimpleImputer`, `StandardScaler`, `OneHotEncoder`, `DummyClassifier`, `LogisticRegression`, `RandomForestClassifier`, metrics), Pandas, NumPy, Matplotlib, Seaborn.

---

### 📅 Week 4: Evaluation, Tuning & Pipelines (In Progress)

#### ✅ Day 1: Building a Three-Way Split (Train / Validation / Test)
* **Objective:** Performing a 60/20/20 Train / Validation / Test split, tuning hyperparameters on the Validation Set only, and evaluating the final model exactly once on the untouched Test Set to prevent data leakage.
* **Key Tasks & Accomplishments:**
  - Generated a synthetic classification dataset (1,000 samples, 10 features) with `make_classification` and a fixed `SEED = 42`.
  - Built the **60/20/20 split** with two chained, stratified `train_test_split` calls — Train+Val (80%) vs Test (20%), then Train (60%) vs Validation (20%): 600 train / 200 validation / 200 test samples.
  - Trained a `DecisionTreeClassifier` baseline on the Training Set and tuned `max_depth` in `[1, 2, 3, 5, 7, 10, 15, None]` using **only the Validation Set** — selected **`max_depth = 15`** (Validation Accuracy **0.8350**), preferring the smaller depth on ties.
  - Retrained the final model on Train + Validation and evaluated it **exactly once** on the untouched Test Set — **Final Test Accuracy 0.7950** (Precision ~0.80, Recall ~0.80, F1 ~0.79).
  - Documented why tuning on the Test Set is dangerous: **optimization bias & test contamination**, **false optimism**, and the role of each split — Train learns weights, Validation selects hyperparameters, Test verifies once.
* **Tools used:** `scikit-learn` (`make_classification`, `train_test_split`, `DecisionTreeClassifier`, `accuracy_score`, `classification_report`), NumPy, Pandas.

#### ✅ Day 2: Cross-Validating a Model (5-Fold Cross-Validation)
* **Objective:** Obtaining an unbiased, reliable performance estimate by evaluating a classification model with 5-Fold Cross-Validation and comparing it against a single train/validation split.
* **Key Tasks & Accomplishments:**
  - Generated a synthetic customer-churn classification dataset (1,000 samples, 10 features, 80% Non-Churn / 20% Churn) with `make_classification` and a fixed `SEED = 42`.
  - Performed **leak-free 5-Fold Cross-Validation** manually — fitting `StandardScaler()` on each training fold only, then `LogisticRegression(random_state=SEED)` — over 5-Fold `StratifiedKFold(n_splits=5, shuffle=True, random_state=SEED)` with the weighted F1 metric (no `Pipeline`).
  - Reported per-fold scores (0.8543, 0.8268, 0.8729, 0.8333, 0.8638) and the **final estimate: Mean F1 0.8502 ± Std 0.0176** — the small standard deviation confirms the model is stable across all folds.
  - Compared the CV mean against a single stratified 80/20 split — **Single-Split F1 0.8227** vs. **CV Mean 0.8502** (difference −0.0275): the single split was slightly pessimistic because that particular 20% hold-out was harder than average, while cross-validation uses every sample for validation exactly once.
  - Visualized the comparison — fold scores vs. CV mean vs. single-split F1 — with Matplotlib.
  - Verified that `scikit-learn` auto-applies `StratifiedKFold` for classification and justified why it matters: plain `KFold` on the imbalanced 80/20 data could produce folds with 5% or 35% minority samples, biasing evaluation or making F1 computation invalid; `StratifiedKFold` preserves the exact class ratio in every fold.
* **Tools used:** `scikit-learn` (`make_classification`, `train_test_split`, `StratifiedKFold`, `KFold`, `StandardScaler`, `LogisticRegression`, `f1_score`), NumPy, Pandas, Matplotlib.

---

## 🛠️ Tech Stack & Tools

* **Language:** Python 3.10+
* **Libraries:** NumPy, Pandas, Matplotlib, Seaborn, scikit-learn, Jupyter
* **Environment:** VS Code, Windows PowerShell / Command Prompt, Git & GitHub

---

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone --recurse-submodules https://github.com/adam-alAj/BinX-ML-Internship.git
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

