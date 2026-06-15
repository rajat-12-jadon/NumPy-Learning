# 🔢 NumPy Notes

## What is NumPy?

NumPy (Numerical Python) is a Python library used for numerical computing and working with multidimensional arrays.

It provides:

* Fast Array Operations
* Mathematical Functions
* Linear Algebra Tools
* Statistical Functions
* Efficient Memory Usage

---

# Importing NumPy

```python
import numpy as np
```

---

# Why NumPy?

Python Lists:

* Slower
* More Memory Usage

NumPy Arrays:

* Faster
* Less Memory Usage
* Optimized for Numerical Computation

---

# 1. Creating NumPy Arrays

## From List

```python
arr = np.array([1,2,3,4,5])
```

---

## 2D Array

```python
arr = np.array([
    [1,2,3],
    [4,5,6]
])
```

---

## Check Type

```python
type(arr)
```

Output:

```text
numpy.ndarray
```

---

# 2. Array Attributes

## Shape

Returns rows and columns.

```python
arr.shape
```

Example:

```text
(2,3)
```

---

## Dimension

```python
arr.ndim
```

Example:

```text
2
```

---

## Size

Total elements.

```python
arr.size
```

---

## Data Type

```python
arr.dtype
```

---

# 3. Special Arrays

## Zeros

```python
np.zeros((3,3))
```

---

## Ones

```python
np.ones((2,2))
```

---

## Identity Matrix

```python
np.eye(3)
```

Output:

```text
1 0 0
0 1 0
0 0 1
```

---

## Full Array

```python
np.full((3,3),5)
```

---

# 4. Creating Sequences

## arange()

Similar to range().

```python
np.arange(0,10)
```

Output:

```text
[0 1 2 3 4 5 6 7 8 9]
```

---

## linspace()

Creates evenly spaced numbers.

```python
np.linspace(0,10,5)
```

Output:

```text
[0.0 2.5 5.0 7.5 10.0]
```

---

# 5. Reshaping Arrays

## reshape()

```python
arr = np.arange(12)

arr.reshape(3,4)
```

Output:

```text
3 rows
4 columns
```

---

# 6. Indexing

## 1D Array

```python
arr[0]
arr[3]
```

---

## 2D Array

```python
arr[1,2]
```

Meaning:

```text
row 1
column 2
```

---

# 7. Slicing

## 1D Slicing

```python
arr[1:5]
```

---

## 2D Slicing

```python
arr[0:2,1:3]
```

Meaning:

```text
rows 0-1
columns 1-2
```

---

# 8. Boolean Masking

Used for filtering.

```python
arr[arr > 5]
```

Example Output:

```text
[6 7 8 9]
```

---

# 9. Array Operations

## Addition

```python
arr + 5
```

---

## Subtraction

```python
arr - 2
```

---

## Multiplication

```python
arr * 3
```

---

## Division

```python
arr / 2
```

---

## Power

```python
arr ** 2
```

---

# 10. Mathematical Functions

## Square Root

```python
np.sqrt(arr)
```

---

## Exponential

```python
np.exp(arr)
```

---

## Absolute Value

```python
np.abs(arr)
```

---

# 11. Statistical Functions

## Sum

```python
np.sum(arr)
```

---

## Mean

```python
np.mean(arr)
```

---

## Median

```python
np.median(arr)
```

---

## Standard Deviation

```python
np.std(arr)
```

---

## Minimum

```python
np.min(arr)
```

---

## Maximum

```python
np.max(arr)
```

---

# 12. Axis Operations

Consider:

```python
arr = np.array([
    [1,2,3],
    [4,5,6]
])
```

---

## Column Wise

```python
np.sum(arr, axis=0)
```

Output:

```text
[5 7 9]
```

---

## Row Wise

```python
np.sum(arr, axis=1)
```

Output:

```text
[6 15]
```

---

# 13. Transpose

Convert rows into columns.

```python
arr.T
```

---

# 14. Flattening Arrays

Convert multi-dimensional array into 1D.

```python
arr.flatten()
```

---

# 15. Unique Values

Returns distinct values.

```python
np.unique(arr)
```

Example:

```python
arr = np.array([1,2,2,3,3,4])

np.unique(arr)
```

Output:

```text
[1 2 3 4]
```

---

# 16. Practical Exercise: Student Dataset

Example:

```python
data = np.array([
    [18,85,78],
    [19,92,88],
    [17,76,95]
])
```

Questions Solved:

### Average Age

```python
np.mean(data[:,0])
```

---

### Math Marks

```python
data[:,1]
```

---

### Highest Science Marks

```python
np.max(data[:,2])
```

---

### Students with Math > 90

```python
data[data[:,1] > 90]
```

---

### Increase Marks

```python
data[:,1] += 5
```

---

### Students Younger Than 19

```python
len(data[data[:,0] < 19])
```

---

# 17. Practical Exercise: Valid Sudoku

Objective:

Check whether a Sudoku board is valid.

Rules:

* Each row contains numbers 1–9 exactly once.
* Each column contains numbers 1–9 exactly once.
* Each 3×3 box contains numbers 1–9 exactly once.

---

## Row Validation

```python
np.sum(row) == 45
len(np.unique(row)) == 9
```

---

## Column Validation

```python
for col in s.T:
```

Using transpose:

```python
s.T
```

Rows become columns.

---

## 3×3 Box Validation

```python
box = s[i:i+3, j:j+3].flatten()
```

Why?

Sudoku requires every 3×3 box to contain:

```text
1 2 3
4 5 6
7 8 9
```

without repetition.

---

# Commonly Used Functions

```python
np.array()

np.zeros()
np.ones()
np.eye()
np.full()

np.arange()
np.linspace()

reshape()

flatten()

np.sum()
np.mean()
np.median()
np.std()

np.min()
np.max()

np.unique()

np.sqrt()
np.exp()
np.abs()
```

---

# Learning Outcome

After completing NumPy fundamentals, you should be able to:

✅ Create and manipulate arrays

✅ Perform indexing and slicing

✅ Apply mathematical operations

✅ Use statistical functions

✅ Filter data using Boolean Masking

✅ Work with multi-dimensional arrays

✅ Solve practical array-based problems

✅ Prepare data for Pandas, Data Analysis, and Machine Learning

---

# NumPy Roadmap Position

```text
Python
   ↓
NumPy ✅
   ↓
Pandas
   ↓
Matplotlib
   ↓
Seaborn
   ↓
Scikit-Learn
   ↓
Machine Learning
```
