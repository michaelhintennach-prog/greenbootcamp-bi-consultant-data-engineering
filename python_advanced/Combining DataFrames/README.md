# Combining DataFrames with Pandas

This module introduces the different ways to combine, join, merge, and concatenate DataFrames in Pandas.  
You learn how each method behaves, when to use it, and how these operations relate to SQL join concepts.

## Objectives
By the end of this module, you will be able to:
- Combine DataFrames using `merge()`, `join()`, and `concat()`
- Understand default behaviors of each method
- Work with categorical variables using `get_dummies()`
- Apply different join types (inner, outer, left, right)
- Combine multiple datasets into a single DataFrame
- Solve practical exercises involving merging and concatenation

## Key Concepts

### 1. Overview of Combining Methods
Pandas provides several ways to combine datasets:

#### `pd.merge()`
- Joins DataFrames on **common columns** by default  
- Very similar to SQL joins  
- Flexible and explicit

#### `df.join()`
- Joins DataFrames on **indices** by default  
- Convenient when index alignment is intended

#### `pd.concat()`
- Stacks DataFrames **vertically (axis=0)** or **horizontally (axis=1)**  
- Does not require matching columns or indices  
- Useful for appending or combining multiple DataFrames

Each method can perform inner, outer, left, or right joins.

### 2. Using `get_dummies()` for Categorical Variables
You convert the wine quality column into dummy variables:

- `pd.get_dummies(wine_df.quality, prefix='quality')`
- Creates one column per category (quality_3, quality_4, …)
- Useful for machine learning and modeling

You then join the dummy DataFrame back to the original using:

- `wine_df.join(quality_dummies)`

### 3. Using `concat()` to Combine DataFrames
You explore horizontal concatenation:

```python
pd.concat([quality_dummies, wine_df], axis=1)
```

This stacks columns side‑by‑side.

### 4. Combining Red and White Wine Data
You compute:

- Mean fixed acidity per quality level for red wines  
- Mean fixed acidity per quality level for white wines  

Then you combine these summary DataFrames using:

#### `merge()`
```python
pd.merge(red_df, white_df, on='quality', suffixes=[' red', ' white'])
```

#### `concat()`
```python
pd.concat([red_df, white_df['fixed acidity']], axis='columns', join='inner')
```

#### `join()`
```python
red_df.join(white_df, lsuffix='red', rsuffix='white')
```

All three approaches produce similar results but differ in defaults and flexibility.

## Exercises & Insights

### Exercise 1: Student Data
You:
- Concatenate two student DataFrames vertically  
- Merge with a third DataFrame containing marks  
- Observe missing names/subjects for students only present in the marks table

**Insight:**  
Outer joins preserve all information, even when some fields are missing.

### Exercise 2: Weather Data
You:
- Merge mean and max temperature data using an outer join  
- Sort months in calendar order  
- Fill missing max temperatures with the average of known values

This demonstrates how merging preserves information and how missing values can be imputed.

## Summary
This module teaches you how to:
- Choose the right method (`merge`, `join`, `concat`) for combining DataFrames  
- Work with categorical variables using dummy encoding  
- Combine datasets with different shapes and keys  
- Apply SQL‑style joins in Pandas  
- Handle missing data after merging  
- Build clean, structured DataFrames from multiple sources  

It provides essential skills for real‑world data engineering and data science workflows.
```

