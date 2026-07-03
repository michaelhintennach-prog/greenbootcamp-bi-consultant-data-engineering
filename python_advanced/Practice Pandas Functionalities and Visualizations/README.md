# Practice Pandas Functionalities and Visualizations (Iris Dataset)

This practice session reinforces Pandas fundamentals and basic visualization techniques using the famous **Iris dataset**.  
The goal is to independently explore, analyze, and visualize the data without step‑by‑step instructions.

## Objectives
By the end of this module, you will be able to:
- Load CSV data into a Pandas DataFrame  
- Inspect and explore tabular data  
- Apply common DataFrame methods (shape, info, describe, filtering, grouping)  
- Compute descriptive statistics (mean, median, mode, variance, standard deviation)  
- Create visualizations using `.plot()`  
- Interpret distributions and relationships  
- Engineer new columns and create filtered subsets  

## Key Concepts

### 1. Data Loading & Inspection
You practice:
- Importing Pandas  
- Reading the Iris dataset (`Iris.csv`)  
- Viewing the first and last rows  
- Checking dataset shape and entry counts  
- Detecting missing values  
- Verifying class balance across species  

### 2. Descriptive Statistics
You compute:
- Mean, median, mode of petal length  
- Minimum and maximum values  
- Variance and standard deviation  
- Full descriptive statistics using `df.describe()`  
- Overall average sepal length  

These steps help understand the distribution and variability of the features.

### 3. Grouping & Aggregation
Using `groupby()`, you determine:
- Count of samples per species  
- Average sepal and petal dimensions per species  

This reveals structural differences between *setosa*, *versicolor*, and *virginica*.

### 4. Feature Engineering
You create new columns:
- `sepal_sum` = sepal length + sepal width  
- `petal_area` = petal length × petal width  

You also generate:
- A filtered DataFrame with petal areas > 1 cm²  
- Three separate DataFrames, one for each species  

### 5. Visualization
You practice multiple plot types:
- Histogram of petal length  
- Scatter plot comparing sepal length vs. sepal width  
- Scatter matrix for petal length and width  

These visualizations help identify:
- Distribution shapes  
- Species clusters  
- Relationships between features  

### 6. Interpretation
You reflect on:
- Whether summary statistics or visualizations are more informative  
- What the distributions reveal about the dataset  
- How species differ visually and numerically  

## Summary
This module strengthens your ability to:
- Explore a dataset independently  
- Combine statistics with visualizations  
- Understand patterns in multivariate data  
- Build new features and filtered subsets  

It serves as a bridge between guided Pandas practice and more advanced exploratory data analysis.

