# Day 1: Python & Data Science Environment Setup

**Date:** Week 1, Day 1  
**Focus:** Establishing a professional, isolated Python data-science environment and Jupyter Notebook & Git workflow.

---

## 📌 Objectives

- Set up a clean, isolated Python virtual environment (`.venv`)
- Install core data science libraries: `numpy`, `pandas`, `matplotlib`, and `jupyter`
- Configure a reproducible project folder structure
- Generate `requirements.txt` and `.gitignore` for dependency tracking and repository cleanliness
- Verify successful installation of all libraries
- Set up Git version control and perform initial commits/pushes to GitHub

---

## 📓 Notebook: `day1.ipynb`

### Content Summary

The notebook contains two sections:

#### 1. Environment Overview (Markdown)
A header cell documenting the purpose of Day 1 — successful setup of the Python data science environment.

#### 2. Library Version Verification (Code)
A code cell that imports the core libraries and prints their installed versions:

```python
import numpy as np
import pandas as pd
import matplotlib as mpl
import jupyter

print("Numpy Version:", np.__version__)      # 2.5.1
print("Pandas Version:", pd.__version__)      # 3.0.3
print("matplotlib Version:", mpl.__version__) # 3.11.1
```

**Output Confirmation:**
| Library    | Version |
|------------|---------|
| NumPy      | 2.5.1   |
| Pandas     | 3.0.3   |
| Matplotlib | 3.11.1  |

---

## 🛠️ Setup Steps Performed

1. **Virtual Environment Creation**
   - Created `.venv` directory using `python -m venv .venv`
   - Activated environment for package isolation

2. **Package Installation**
   - Installed `numpy`, `pandas`, `matplotlib`, and `jupyter` via `pip`
   - Ensured compatible versions for the Python 3.14 runtime

3. **Project Structuring**
   - Organized the repository into logically separated weekly and daily folders (`week1/Day1/`, `week1/Day2/`, etc.)
   - Configured `.gitignore` to exclude virtual environments, cache files, and checkpoints

4. **Dependency Management**
   - Generated `requirements.txt` with pinned versions for complete reproducibility

5. **GitHub Integration**
   - Initialized Git repository and connected to remote (`origin/main`)
   - Pushed initial commits to document the starting point

---

## ✅ Key Outcomes

- Fully functional isolated Python environment for data science
- All core numerical and data analysis libraries installed and verified
- Project structure ready for scalable daily labs
- Git-based version control workflow established

---

## 🔗 Related Files

- [`day1.ipynb`](./day1.ipynb) — Main notebook
- [`../../requirements.txt`](../../requirements.txt) — Project-wide pinned dependencies
- `../../.gitignore` — Repository exclusion rules
