# Analyzing Ride-Sharing Patterns: Insights for Zuber

## Project Overview

This project explores ride-sharing trends in Chicago to help **Zuber**, a ride-sharing company, better understand customer behavior and optimize service delivery. The analysis focuses on identifying high-demand neighborhoods, top-performing taxi companies, and the impact of weather on trip duration.

## Project Objectives

The main objectives of this analysis are:
1. Identify neighborhoods with the highest ride demand.
2. Analyze the most active taxi companies by ride volume.
3. Understand how weather conditions influence trip durations.
4. Test hypotheses to validate assumptions using statistical methods.

## Features

### 1. Data Preparation
- Load and inspect datasets related to taxi companies, drop-off neighborhoods, and specific trips between Loop and O'Hare.
- Convert time columns and handle duplicates thoughtfully (e.g., grouped by hour).
- Enrich data with calculated fields such as market share.

### 2. Exploratory Data Analysis
- Visualize top neighborhoods for drop-offs.
- Identify key taxi companies dominating the market.
- Create bar charts and box plots using Plotly for clear insights.

### 3. Hypothesis Testing
- Test if **ride durations differ on rainy vs. non-rainy Saturdays** using a two-sample t-test.
- Visualize duration differences with a box plot.

## Technologies Used

- **Python**: Main programming language
- **Pandas**: Data manipulation
- **NumPy**: Numerical operations
- **SciPy**: Statistical testing
- **Plotly Express**: Interactive visualizations
- **Jupyter Notebook**: Analysis environment

## Dataset

Three datasets were used:
- `project_sql_result_01.csv`: Taxi company names and number of trips.
- `project_sql_result_04.csv`: Drop-off neighborhoods and average trips.
- `project_sql_result_07.csv`: Rides from Loop to O'Hare with weather and duration info.

## Analysis Workflow

### 1. Initialization & Loading
- Import libraries, load CSVs, inspect initial structure.

### 2. Data Cleaning
- Convert time columns to datetime.
- Check and assess duplicates.
- Add new features (e.g., market share).

### 3. Exploratory Data Analysis
- Visualize top 10 drop-off neighborhoods.
- Highlight top 10 taxi companies.

### 4. Hypothesis Testing
- Compare ride durations on rainy vs. non-rainy Saturdays using `scipy.stats.ttest_ind`.

## Key Findings

1. **The Loop, River North, and Streeterville** had the highest ride drop-offs, suggesting central business/residential hubs.
2. A few companies, especially **Flash Cab**, dominate the ride volume market.
3. **Rainy weather significantly increases trip duration** from Loop to O'Hare on Saturdays.

## Recommendations

1. **Increase Zuber coverage** in high-demand areas during peak hours.
2. **Study strategies of top taxi companies** (pricing, availability).
3. Prepare for **weather-related delays** with dynamic routing or pricing adjustments.

## Project Structure

- `ride_share_analysis.ipynb`: Jupyter Notebook with full analysis and visualizations.
- `datasets/`
    - `project_sql_result_01.csv`
    - `project_sql_result_04.csv`
    - `project_sql_result_07.csv`
- `README.md`: Project summary and findings.