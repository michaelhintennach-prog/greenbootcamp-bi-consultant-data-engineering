# Introduction to NumPy

NumPy is one of the core libraries for scientific computing in Python.  
It provides the **ndarray**, a fast, memory‑efficient data structure that forms the foundation of many other libraries — including Pandas.  
Understanding NumPy is essential for efficient numerical operations, vectorization, and array‑based computation.

## Objectives
By the end of this module, you will:
- Understand what makes NumPy arrays special  
- Create and inspect NumPy arrays  
- Perform mathematical operations and broadcasting  
- Index and slice multidimensional arrays  
- Use aggregation methods (sum, mean, std, min, max, argmin, argmax)  
- Work with array reshaping, flattening, cumulative operations  
- Use `np.where()` for conditional indexing  
- Create pivot tables in Pandas using NumPy concepts  

---

## Why NumPy Arrays Are Special

NumPy arrays are significantly faster than Python lists because:

### 1. **Contiguous Memory Layout**
All elements are stored in one continuous block → enables vectorized CPU operations.

### 2. **Homogeneous Data Types**
All elements share the same type → no repeated type‑checking → faster computation.

### Performance Example
Summing 1,000,000 numbers:
- `np.sum()` on a NumPy array is **much faster** than Python’s built‑in `sum()`  
- Using Python’s `sum()` on a NumPy array is slower because it breaks vectorization

---

## Creating NumPy Arrays

### Basic Constructor
```python
np.array([10, 20, 30])
np.array((10, 20, 30), dtype=np.int32)

