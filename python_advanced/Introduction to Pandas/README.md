# Introduction to Pandas

Pandas is one of the core libraries for data analysis in Python. It provides the **DataFrame**, a powerful tabular data structure that allows efficient data loading, exploration, manipulation, and preparation for further analysis or machine learning.

## Key Concepts

### DataFrames & Series
A DataFrame consists of rows and columns, with each column represented as a Series. It is the main structure used for working with tabular data.

### Creating DataFrames
You can create DataFrames from:
- Lists of dictionaries  
- Lists of lists with column names  
- External files using `pd.read_*` (CSV, JSON, Excel, SQL, HTML)

### Exploring Data
Common inspection methods include:
- `df.head()` and `df.tail()` for previewing data  
- `df.shape` for dimensions  
- `df.columns` for column names  
- `df.info()` for data types  
- `df.describe()` for statistical summaries

### Indexing & Selecting Data
- Column selection: `df['col']` or `df.col`  
- Row slicing: `df[start:end]`  
- Label-based selection: `df.loc[]`  
- Position-based selection: `df.iloc[]`

### Filtering & Querying
- Boolean filtering: `df[df['Length'] > 0.4]`  
- Combined conditions using `&` and `|`  
- Readable filtering with `df.query()`

### Data Cleaning
- Handling missing values: `fillna()`, `dropna()`  
- Renaming columns: `df.rename()`  
- Creating new columns: `df.eval()`  
- Dropping columns: `df.drop()`

### Grouping & Aggregation
- `df.groupby()` for split–apply–combine workflows  
- Aggregations like `.mean()`, `.max()`, `.count()`  
- Grouping by multiple columns

### Sorting
- `df.sort_values()` for ordering data by one or more columns

## What We Learned
- How to load, inspect, and understand tabular data  
- How to select, filter, and transform data  
- How to handle missing values  
- How to aggregate and sort data  
- How to engineer new features inside a DataFrame
