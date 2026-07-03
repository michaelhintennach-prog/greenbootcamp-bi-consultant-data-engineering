## Introduction to NumPy

NumPy is one of the core libraries for scientific computing in Python. Pandas DataFrames are built on top of NumPy arrays, so understanding NumPy helps you understand what happens under the hood when working with tabular data.

NumPy arrays are significantly faster than Python lists because:
- They store data in one contiguous block of memory.
- All elements share the same data type, enabling vectorized operations.

Vectorization allows the CPU to apply one operation to many elements at once, making numerical computations extremely efficient.

## Objectives
By the end of this module, you will:
- Create NumPy arrays.
- Understand key NumPy functionality.
- Know when and why NumPy arrays are useful.

## Creating NumPy Arrays

You can create arrays using `np.array()` from lists or tuples. Arrays have attributes such as:
- `.shape` — the dimensions of the array
- `.dtype` — the data type of the elements

NumPy enforces homogeneity. If you mix types, NumPy will cast everything to a common type (often strings or floats). If casting fails, NumPy raises an error.

NumPy also provides convenient constructors:
- `np.zeros()`
- `np.ones()`
- `np.identity()`
- `np.random.rand()`
- `np.arange()`

## Mathematical Operations

NumPy supports element‑wise operations using standard operators (`+`, `-`, `*`, `/`, `%`, `**`). Operations between arrays of the same shape are applied element‑wise.

Operations between arrays and single values use **broadcasting**, which automatically expands the scalar to match the array’s shape.

Broadcasting also works for row‑wise or column‑wise operations by aligning shapes appropriately.

## Indexing and Slicing

NumPy arrays behave like multidimensional lists. You index them using standard Python indexing:
- `arr[row, column]`
- `arr[:, 1]` → all rows, column 1
- `arr[0:2]` → first two rows
- `arr[0:3, 1:4]` → sub‑matrix slicing

Arrays can be reshaped using `.reshape()`.

## Aggregations and Statistics

NumPy provides fast aggregation methods:
- `arr.sum()`
- `arr.mean()`
- `arr.std()`
- `arr.max()`
- `arr.min()`

You can compute these along rows or columns using `axis=0` or `axis=1`.

To get the index of min/max values:
- `arr.argmin()`
- `arr.argmax()`

## Additional Array Methods

Useful operations include:
- `arr.cumsum()` — cumulative sum
- `arr.cumprod()` — cumulative product
- `arr.flatten()` — returns a 1D copy
- `arr.ravel()` — returns a flattened view

## Summary

NumPy arrays are fast, memory‑efficient, homogeneous, and ideal for numerical and scientific computing. They support vectorized operations, broadcasting, slicing, reshaping, and a wide range of mathematical and statistical methods. Understanding NumPy is essential for effective data manipulation and forms the foundation for libraries like Pandas.

