# Day 5: Data Visualization Mini-Project & Exploratory Data Analysis

**Date:** Week 1, Day 5  
**Focus:** Integrating all Week 1 skills (NumPy, Pandas, Matplotlib) to perform exploratory data analysis and visual communication using the MPG automobile dataset.

---

## 📌 Objectives

- Load and process a real-world dataset using Pandas and NumPy
- Generate four key Matplotlib visualizations: Line Plot, Scatter Plot, Bar Plot, and Histogram
- Combine multiple charts into a structured 2×2 Subplots grid
- Document all findings with proper labels, legends, and annotations

---

## 📓 Notebook: `Data_Visualization_Mini_Project.ipynb`

### Step 1: Library Imports & Setup

**What was done:**  
Imported the core data science stack — NumPy, Pandas, and Matplotlib — and set a reproducible random seed (`np.random.seed(42)`). The `seaborn-v0_8-whitegrid` style was configured for clean, publication-ready plots.

**Code highlights:**
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

np.random.seed(42)
plt.style.use('seaborn-v0_8-whitegrid')
```

**Why it matters:**  
Reproducibility (fixed seed) and visual consistency (style config) are hallmarks of professional data science work.

---

### Step 2: Data Loading & Feature Engineering

**What was done:**  
Loaded the **MPG automobile dataset** (398 cars, 9 columns) directly from the official Seaborn GitHub repository. Two new features were engineered using vectorized NumPy operations:

1. **kpl (Kilometers Per Liter):** Converted from MPG (`1 mpg = 0.425144 kpl`)
2. **efficiency_category:** Binned MPG values into three classes using `np.select()`:
   - `High Efficiency` (mpg ≥ 25)
   - `Medium Efficiency` (18 ≤ mpg < 25)
   - `Low Efficiency` (mpg < 18)

Missing `horsepower` values were imputed with the median.

**Code highlights:**
```python
data_url = "https://raw.githubusercontent.com/mwaskom/seaborn-data/master/mpg.csv"
df_mpg = pd.read_csv(data_url)

# Vectorized KPL conversion
df_mpg['kpl'] = np.round(df_mpg['mpg'].values * 0.425144, 2)

# Vectorized efficiency classification
conditions = [df_mpg['mpg'].values >= 25,
              (df_mpg['mpg'].values >= 18) & (df_mpg['mpg'].values < 25),
              df_mpg['mpg'].values < 18]
choices = ['High Efficiency', 'Medium Efficiency', 'Low Efficiency']
df_mpg['efficiency_category'] = np.select(conditions, choices)
```

---

### Compute Statistics (NumPy Deep-Dive)

**What was done:**  
Extracted `weight` and `horsepower` as raw NumPy arrays and computed key statistical metrics: mean, standard deviation, percentiles (25th, 75th), and Interquartile Range (IQR).

**Key Findings:**

| Metric           | Weight (lbs) | Horsepower (HP) |
|------------------|:------------:|:---------------:|
| Mean             | 2970.42      | 104.30          |
| Std Dev          | 845.78       | 38.17           |
| 25th Percentile  | 2223.75      | 76.00           |
| 75th Percentile  | 3608.00      | 125.00          |
| IQR              | 1384.25      | 49.00           |

**Interpretation:**  
- Weight distribution is right-skewed — some very heavy US cars pull the mean above the median.
- Horsepower shows moderate spread; the IQR of 49 HP indicates a wide performance range across vehicle origins.

---

### Step 3: Line Plot — MPG Trend Over Time

**What was done:**  
Plotted the average MPG per `model_year` to visualize the historical improvement in fuel efficiency from 1970 to 1982.

**Key Observations:**
- Average MPG rose from **~17 MPG (1970)** to **~30 MPG (1982)** — an ~76% increase.
- The sharpest gains occurred after the **1973 oil crisis** and **1979 energy crisis**, reflecting regulatory shifts (CAFE standards).

**Code highlights:**
```python
yearly_mpg = df_mpg.groupby('model_year')['mpg'].mean()
plt.plot(yearly_mpg.index, yearly_mpg.values, marker='o', color='#2E86AB')
plt.title('Average MPG Over Model Years')
plt.xlabel('Model Year')
plt.ylabel('Average MPG')
plt.grid(True, alpha=0.3)
```

---

### Step 4: Scatter Plot — Weight vs. MPG

**What was done:**  
Created a scatter plot to examine the relationship between vehicle weight and fuel efficiency, colored by manufacturing origin (USA, Europe, Japan).

**Key Observations:**
- **Strong negative correlation** between weight and MPG — lighter cars are more fuel-efficient.
- **Japanese cars** cluster in the low-weight, high-MPG region.
- **US cars** dominate the high-weight, low-MPG region.
- **European cars** occupy a middle ground — moderate weight with good efficiency.

**Code highlights:**
```python
colors = {'usa': '#A63446', 'europe': '#F2C14E', 'japan': '#2E86AB'}
plt.scatter(df_mpg['weight'], df_mpg['mpg'],
            c=df_mpg['origin'].map(colors), alpha=0.6)
plt.xlabel('Weight (lbs)')
plt.ylabel('MPG')
plt.title('Weight vs. MPG by Origin')
```

---

### Step 5: Bar Plot — Average MPG by Origin

**What was done:**  
Computed and visualized the mean MPG for each manufacturing region using a bar chart with error bars (standard deviation).

**Key Observations:**

| Origin  | Avg MPG | Avg HP | Avg Weight | Count |
|---------|:-------:|:------:|:----------:|:-----:|
| Japan   | 30.45   | 79.84  | 2,221      | 79    |
| Europe  | 27.89   | 80.93  | 2,423      | 70    |
| USA     | 20.08   | 118.64 | 3,362      | 249   |

- **Japan leads** in fuel efficiency (~30.45 MPG avg) with lighter cars and lower horsepower.
- **USA** has the lowest average MPG (~20.08) due to heavier vehicles and higher horsepower.
- European cars offer a balanced trade-off between performance and efficiency.

**Code highlights:**
```python
origin_stats = df_mpg.groupby('origin')['mpg'].agg(['mean', 'std']).reset_index()
plt.bar(origin_stats['origin'], origin_stats['mean'],
        yerr=origin_stats['std'], capsize=5, color=['#A63446', '#F2C14E', '#2E86AB'])
plt.ylabel('Average MPG')
plt.title('Average MPG by Manufacturing Origin')
```

---

### Step 6: Histogram — MPG Distribution

**What was done:**  
Plotted the distribution of MPG values across all 398 car models using a histogram with density curve overlay.

**Key Observations:**
- **Bimodal distribution:** Two peaks — one around **15–18 MPG** (mostly US cars) and another around **27–33 MPG** (mostly Japanese and European cars).
- The gap between these peaks reflects the division between performance-oriented (heavy) and economy-oriented (light) vehicles.

**Code highlights:**
```python
plt.hist(df_mpg['mpg'], bins=15, density=True, alpha=0.7, color='#2E86AB', edgecolor='white')
plt.xlabel('MPG')
plt.ylabel('Density')
plt.title('Distribution of MPG Values')
```

---

### Step 7: Combined 2×2 Subplots Grid

**What was done:**  
Merged all four visualizations into a single publication-ready 2×2 figure using `plt.subplots()`.

```python
fig, axes = plt.subplots(2, 2, figsize=(14, 10))
fig.suptitle('MPG Automobile Dataset — Exploratory Data Analysis', fontsize=16, fontweight='bold')

# Plot 1: Line Chart — MPG Over Years
axes[0, 0].plot(...)

# Plot 2: Scatter Plot — Weight vs MPG
axes[0, 1].scatter(...)

# Plot 3: Bar Chart — Avg MPG by Origin
axes[1, 0].bar(...)

# Plot 4: Histogram — MPG Distribution
axes[1, 1].hist(...)

plt.tight_layout()
plt.show()
```

---

## 🔍 Final Insights

1. **Fuel efficiency improved dramatically** from 1970 (~17 MPG) to 1982 (~30 MPG), driven by oil crises and regulatory changes.
2. **Weight is the strongest predictor** of fuel economy — lighter cars consistently achieve higher MPG.
3. **Japanese manufacturers** lead in efficiency (30.45 MPG avg), while **US manufacturers** lag (20.08 MPG avg) due to heavier, more powerful vehicles.
4. **European cars** strike a balance between performance and economy (~27.89 MPG avg).
5. The **bimodal MPG distribution** reveals two distinct market segments: economy cars and performance/utility vehicles.

---

## ✅ Skills Reinforced

| Skill | Application |
|-------|-------------|
| **NumPy** | Vectorized KPL conversion, efficiency classification, statistical metrics (mean, std, percentiles, IQR) |
| **Pandas** | Data loading, `.groupby()`, `.agg()`, `.to_numpy()`, missing value imputation |
| **Matplotlib** | Line plots, scatter plots, bar plots, histograms, subplots (2×2 grid), labels, legends, color mapping |
| **EDA** | Trend analysis, correlation identification, distribution analysis, categorical comparison |
| **Storytelling** | Communicating data-driven insights through visual narratives |

---

## 🔗 Related Files

- [`Data_Visualization_Mini_Project.ipynb`](./Data_Visualization_Mini_Project.ipynb) — Main notebook with all visualizations
