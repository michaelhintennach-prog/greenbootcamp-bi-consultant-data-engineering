# Pandas Practice 3

This practice session focuses on applying Pandas to explore a real‑world dataset (`bike_share_data.csv`).  
The goal is to strengthen your ability to analyze data independently, write efficient chained commands, and extract insights through both statistics and visualizations.

## Objectives
By the end of this module, you will be able to:
- Explore and understand a dataset using Pandas  
- Clean and standardize column names  
- Analyze categorical variables and their frequencies  
- Create pie charts and bar charts with Pandas  
- Identify common and rare values in columns  
- Use `pd.crosstab()` to build contingency tables with margins  
- Investigate trip durations and interpret unusual patterns  
- Engineer new features and clean text fields  
- Perform guided and unguided exploratory data analysis (EDA)

## Key Concepts

### 1. Data Loading & Initial Exploration
You begin by:
- Importing Pandas  
- Loading the bike share dataset  
- Checking the number of observations  
- Inspecting column names and converting them to Pythonic format  
  - lowercase  
  - spaces → `_`  
  - `#` → `num`

### 2. Subscription Type Analysis
You explore:
- Number of subscription types  
- Frequency of each type  
- Pie chart and bar chart visualizations  

This helps understand user segmentation in the bike share system.

### 3. Station Frequency Analysis
You identify:
- Top 10 most frequent start stations  
- Bottom 10 least frequent end stations  

This reveals usage patterns and potential operational hotspots.

### 4. Crosstab Analysis
Using `pd.crosstab()`, you create:
- A table of start stations segmented by subscription type  
- Row and column totals (margins)  

This provides a structured view of user behavior across stations.

### 5. Trip Duration Investigation
You analyze:
- Units of measurement  
- Shortest trips and their counts  
- Longest trips  
- Definition and count of “long” trips  
- Interpretation of unusually long durations  

You reflect on:
- Possible user behavior  
- Data quality issues  
- Operational insights  

### 6. Visualizing Duration
You:
- Plot the duration column  
- Evaluate whether the plot reveals insights  
- Create filtered subsets to improve interpretability  

### 7. Text Cleaning for Station Names
You standardize station names:
- lowercase  
- spaces → `_`  

Example:  
`South Van Ness at Market` → `south_van_ness_at_market`

### 8. Timeboxed Exploration
You finish with a 15‑minute unguided exploration session to:
- Form hypotheses  
- Test ideas  
- Discover patterns without predefined questions  

This simulates real‑world data exploration workflows.

## Summary
This module strengthens your ability to:
- Clean and prepare data  
- Analyze categorical and numerical variables  
- Visualize distributions and frequencies  
- Build contingency tables  
- Interpret unusual patterns  
- Explore data independently and efficiently  

It prepares you for more advanced EDA and real‑world data analysis tasks.

