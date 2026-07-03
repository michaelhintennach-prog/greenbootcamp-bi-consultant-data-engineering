# Seaborn Data Visualization

Seaborn is a powerful Python library for statistical data visualization.  
It builds on top of Matplotlib and provides cleaner aesthetics, better defaults, and high‑level functions for exploring relationships and distributions in data.

This module introduces Seaborn from basic usage to more advanced multi‑plot techniques using the Iris dataset.

## Objectives
By the end of this module, you will be able to:
- Understand Seaborn’s purpose and dependencies  
- Create basic and advanced plots using Seaborn  
- Customize plot styles, themes, and figure sizes  
- Combine Seaborn with Matplotlib for fine‑grained control  
- Use Seaborn’s multi‑plot tools (FacetGrid, PairGrid)  
- Create relational, categorical, and statistical plots  

## Key Concepts

### 1. Introduction to Seaborn
Seaborn provides:
- Beautiful default styles  
- Statistical plotting functions  
- Easy integration with Pandas DataFrames  
- Compatibility with Matplotlib  

You begin by loading the Iris dataset and creating a simple line plot using `sns.lineplot()`.

### 2. Using Seaborn with Matplotlib
Seaborn plots can be customized using Matplotlib functions:
- Adding titles (`plt.title()`)  
- Adjusting axis limits (`plt.xlim()`, `plt.ylim()`)  
- Changing figure size (`plt.figure(figsize=...)`)  
- Removing spines (`sns.despine()`)

This combination gives you both simplicity and flexibility.

### 3. Styling Seaborn Plots
Seaborn provides built‑in themes via `sns.set_style()`:
- `darkgrid`  
- `whitegrid`  
- `dark`  
- `white`  
- `ticks`

You also learn how to:
- Temporarily apply styles using `sns.axes_style()`  
- Customize layout with subplots  

### 4. Multiple Plots
You explore several ways to create multi‑plot layouts:

#### Using Matplotlib
- `add_axes()`  
- `subplot()`  
- `subplot2grid()`  

These allow precise control over subplot placement.

#### Using Seaborn
Seaborn provides higher‑level multi‑plot tools:

##### **FacetGrid**
- Visualizes subsets of data across rows, columns, or hue  
- Ideal for comparing distributions across categories  

##### **PairGrid**
- Shows pairwise relationships between multiple variables  
- Supports different plot types for upper, lower, and diagonal panels  

### 5. Plot Types in Seaborn

#### Relational Plots
Used to visualize relationships between variables.

- `relplot()` — general relational plot interface  
- `scatterplot()` — joint distribution of two variables  
- `lineplot()` — trends and confidence intervals  

#### Categorical Plots
Used when one variable is categorical.

- `barplot()` — mean values per category  
- `countplot()` — frequency counts  
- `boxplot()` — distribution with quartiles and outliers  

These plots help compare species in the Iris dataset.

## Summary
This module teaches you how to:
- Use Se
