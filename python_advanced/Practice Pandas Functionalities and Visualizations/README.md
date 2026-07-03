# Pandas Visualization

This module introduces basic data visualization using Pandas’ built‑in `.plot()` functionality.  
Although Pandas relies internally on **Matplotlib**, it provides a convenient interface for quickly creating common plot types.  
The notebook uses the *red wine quality dataset* to demonstrate how to visualize distributions, relationships, and patterns in tabular data.

## Objectives
By the end of this module, you will be able to:
- Create plots using the Pandas `.plot()` method  
- Understand and use different plot types (histogram, scatter plot, bar plot, box plot)  
- Interpret visualizations to draw meaningful conclusions about the data  

## Key Concepts

### 1. Plotting with Pandas
Pandas allows you to call `.plot()` directly on Series or DataFrames.  
The most important argument is `kind`, which defines the plot type:
- `kind='hist'` — histograms  
- `kind='scatter'` — scatter plots  
- `kind='bar'` — bar charts  
- `kind='box'` — box plots  

### 2. Exploring Distributions
Using histograms, you visualize how values are distributed.  
Example insight from the wine dataset:
- Wine quality scores range from 3 to 8  
- Score **5** is most common (nearly 700 wines)

### 3. Exploring Relationships
Scatter plots help identify relationships between variables:
- Example: `total sulfur dioxide` vs. `free sulfur dioxide`  
- Useful for spotting correlations, clusters, or outliers

### 4. Dataset Overview
The dataset contains 11 input variables (acidity, sugar, chlorides, sulfur dioxide, density, pH, sulphates, alcohol)  
and one output variable:
- **quality** (score from 0 to 10)

These variables can be visualized individually or in combination to understand patterns in wine chemistry.

## Summary
This module provides a first look at visualizing data directly with Pandas.  
You learn how to:
- Generate quick plots for exploration  
- Compare variables visually  
- Interpret distributions and relationships  
- Prepare for more advanced visualizations using Seaborn and Matplotlib

It serves as a foundation for deeper EDA and more sophisticated plotting techniques in later modules.
