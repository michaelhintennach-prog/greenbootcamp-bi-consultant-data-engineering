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

