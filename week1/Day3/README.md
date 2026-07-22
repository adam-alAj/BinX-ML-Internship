# Day 3: NumPy — Numerical Computing & Vectorized Operations

**Date:** Week 1, Day 3  
**Focus:** Building fluency in multi-dimensional numerical computing using NumPy — vectorized operations, indexing, boolean masking, and broadcasting.

---

## 📌 Objectives

- Create and inspect 1D and 2D arrays using various initialization methods
- Perform precise multi-dimensional slicing and indexing
- Replace explicit Python loops with vectorized operations for performance
- Apply boolean masking to filter array data conditionally
- Understand and apply NumPy broadcasting rules

---

## 📓 Notebook: `NumPy_Fundamentals.ipynb`

### Section 1: Array Creation & Inspection

**What was done:**  
Imported NumPy and created a 2D array with shape `(4, 4)` containing values from 1 to 16. Inspected key metadata attributes.

**Code highlights:**
```python
import numpy as np
arr_2d = np.arange(1, 17).reshape(4, 4)

print(arr_2d.shape)  # (4, 4)
print(arr_2d.dtype)  # int64
print(arr_2d.ndim)   # 2
```

**Output:**
```
---2D Array---
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]
 [13 14 15 16]]

Array shape: (4, 4)
Data type: int64
Number of Dimensions: 2
```

**Why it matters:**  
Understanding array shapes and data types is critical before performing any numerical operation — especially when feeding data into ML models that expect specific tensor shapes.

---

### Section 2: Array Slicing & Indexing

**What was done:**  
Demonstrated slicing operations on a 2D array:
- Extracting the **second column** using `arr_2d[:, 1]`
- Extracting the **last row** using `arr_2d[-1, :]`
- Extracting a **2×2 center sub-matrix** using `arr_2d[1:3, 1:3]`

**Code highlights:**
```python
second_column = arr_2d[:, 1]          # [ 2  6 10 14]
last_row = arr_2d[-1, :]              # [13 14 15 16]
center_subMatrix = arr_2d[1:3, 1:3]   # [[ 6  7]
                                      #  [10 11]]
```

**Why it matters:**  
Row/column slicing is a daily operation in data preprocessing — extracting feature subsets, selecting time windows, or splitting train/test data.

---

### Section 3: Boolean Masking & Vectorized Operations

**What was done:**  
Computed statistical metrics (`mean`, `sum`, `std`) using built-in NumPy methods, then applied a boolean mask to filter values greater than the mean — all without any explicit Python loops.

**Code highlights:**
```python
mean_value = arr_2d.mean()   # 8.5
sum_value = arr_2d.sum()     # 136
std_value = arr_2d.std()     # 4.61

mask = arr_2d > mean_value
filtered_values = arr_2d[mask]  # [ 9 10 11 12 13 14 15 16]
```

**Output:**
| Metric | Value |
|--------|-------|
| Mean   | 8.5   |
| Sum    | 136   |
| Std    | 4.61  |

**Why it matters:**  
Vectorized operations run at C speed (not Python speed), making NumPy orders of magnitude faster than native Python loops for large datasets. Boolean masking enables elegant, efficient conditional filtering.

---

### Section 4: NumPy Broadcasting

**What was done:**  
Added a 1D row vector `[10, 20, 30, 40]` (shape `(4,)`) to the 2D array (shape `(4, 4)`) using broadcasting — NumPy automatically stretched the 1D vector across all rows.

**Code highlights:**
```python
row_vector = np.array([10, 20, 30, 40])
broadcasted_result = arr_2d + row_vector

# Original:    [[ 1  2  3  4], ...]
# Vector:      [10 20 30 40]
# Result:      [[11 22 33 44], ...]
```

**Output:**
```
Result after Broadcasting:
[[11 22 33 44]
 [15 26 37 48]
 [19 30 41 52]
 [23 34 45 56]]
```

**Why it matters:**  
Broadcasting eliminates the need for explicit replication loops, saving memory and improving performance — essential when normalizing datasets, adding bias terms, or applying element-wise operations across mismatched shapes.

---

## ✅ Key Takeaways

- `np.arange()` + `.reshape()` is a fast way to create multi-dimensional test arrays
- Multi-dimensional slicing uses the `[rows, cols]` syntax with standard Python slice notation
- NumPy's built-in statistical methods (`mean`, `sum`, `std`) operate **element-wise** by default
- Boolean masks provide a clean, efficient way to filter data without loops
- Broadcasting enables arithmetic between arrays of different shapes without explicit memory duplication
- Always use fixed random seeds (`np.random.seed()`) for reproducibility

---

## 🔗 Related Files

- [`NumPy_Fundamentals.ipynb`](./NumPy_Fundamentals.ipynb) — Main notebook
