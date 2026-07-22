# Day 2: Python Fundamentals for Data Science & OOP

**Date:** Week 1, Day 2  
**Focus:** Mastering clean, idiomatic Python code — data types, control flow, functions, list comprehensions, and Object-Oriented Programming (OOP).

---

## 📌 Objectives

- Understand and apply primitive data types (`int`, `float`, `str`, `bool`) and composite structures (`list`, `tuple`, `dict`, `set`)
- Implement conditional control flow (`if`/`elif`/`else`) and iteration (`for` loops)
- Write reusable functions with type hints and docstrings
- Transform traditional loops into concise list comprehensions
- Build custom classes encapsulating data and behavior (OOP)
- Perform a hands-on data cleaning and summary statistics drill

---

## 📓 Notebook: `Python_Fundamentals.ipynb`

### Part 1: Data Types & Control Flow

**What was done:**  
Defined primitive data types and composite data structures, then used conditional logic and a `for` loop to iterate over a list of skills.

**Code highlights:**
```python
age = 21          # int
height = 1.76     # float
name = "Adam Alafandi"  # str
is_active = True  # bool
skills = ["Python", "Git", "Java"]  # list

score = 85
if score >= 90:
    print("Excellent")
elif score >= 75:
    print("Very Good")     # → "Very Good"

for skill in skills:
    print(f"Skill : {skill}")
```

**Why it matters in Data Science:**  
Lists and dictionaries form the core foundation for handling raw data records, feature sets, and JSON-like APIs before feeding into NumPy arrays or Pandas DataFrames.

---

### Part 2: Functions with Type Hints

**What was done:**  
Defined `calculate_grade()` — a reusable function with explicit type annotations (`score: float → str`) and a standard docstring.

**Code highlights:**
```python
def calculate_grade(score: float) -> str:
    """a function to calculate grades"""
    if score >= 90:
        print("A")
    elif score >= 80:
        print("B")
    else:
        print("C")

print(calculate_grade(88))  # → B
```

**Why it matters in Data Science:**  
Modular functions prevent code duplication and enforce clean code practices. In ML pipelines, encapsulating preprocessing steps inside well-documented functions ensures maintainability and reusability.

---

### Part 3: List Comprehensions

**What was done:**  
Compared a traditional `for` loop with a single-line list comprehension to filter and extract even numbers from a list.

**Code highlights:**
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Traditional way
evens_traditional = []
for num in numbers:
    if num % 2 == 0:
        evens_traditional.append(num)

# List comprehension way
evens_comprehension = [num for num in numbers if num % 2 == 0]
# Both produce: [2, 4, 6, 8, 10]
```

**Why it matters in Data Science:**  
List comprehensions produce cleaner, more readable, and faster code — heavily used for quick feature transformation, filtering invalid values, and flattening nested structures.

---

### Part 4: Object-Oriented Programming (OOP)

**What was done:**  
Created a `DataRecord` class that encapsulates `record_id` and `value` attributes with a `display_info()` method.

**Code highlights:**
```python
class DataRecord:
    def __init__(self, record_id: int, value: float):
        self.record_id = record_id
        self.value = value
    def display_info(self):
        return f"Record id: {self.record_id}, value: {self.value}"

record1 = DataRecord(101, 45.5)
print(record1.display_info())  # → Record id: 101, value: 45.5
```

**Why it matters in Data Science:**  
OOP is the core architecture behind major ML frameworks (Scikit-Learn, PyTorch, TensorFlow). Understanding OOP enables building custom transformers, neural network layers, and modular ML pipelines.

---

### Part 5: Hands-On Lab Drill

**What was done:**  
Combined all Day 2 concepts into an end-to-end mini workflow:
1. Defined `analyze_dataset()` to compute `mean`, `min`, and `max` statistics
2. Used list comprehension to filter out negative measurements (noise)
3. Executed statistical analysis on the cleaned dataset

**Code highlights:**
```python
def analyze_dataset(data: list) -> dict:
    return {
        "mean": sum(data) / len(data),
        "min": min(data),
        "max": max(data)
    }

raw_measurements = [12.5, -4.0, 45.0, 88.2, 102.1, -15.0, 63.4]
clean_measurements = [val for val in raw_measurements if val >= 0]
stats = analyze_dataset(clean_measurements)
```

**Output:**
| Metric | Value  |
|--------|--------|
| Mean   | 62.24  |
| Min    | 12.50  |
| Max    | 102.10 |

**Why it matters in Data Science:**  
Generating baseline descriptive statistics and cleaning noisy data are fundamental steps in Exploratory Data Analysis (EDA) prior to applying ML models.

---

## ✅ Key Takeaways

- Python's built-in data structures are foundational for handling raw data before specialized library processing
- Type hints and docstrings enforce code quality and self-documenting practices
- List comprehensions offer a concise, performant alternative to traditional loops
- OOP principles mirror the architecture of real-world ML frameworks
- Data cleaning + summary statistics is the first step in any data science pipeline

---

## 🔗 Related Files

- [`Python_Fundamentals.ipynb`](./Python_Fundamentals.ipynb) — Main notebook
