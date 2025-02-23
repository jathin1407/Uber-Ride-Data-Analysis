# Uber Rides Data Analysis

## Project Overview
This project aims to analyze Uber ride data to understand ride usage patterns across various categories, purposes, months, days, and times. The analysis is visualized through dashboards and Python visualizations to provide insights that can help make data-driven decisions.

## Files in the Project
- **UberDataset.csv**: The original dataset containing raw Uber ride data.
- **UberDatasetCleaned.csv**: The cleaned dataset after preprocessing.
- **Dashboard.png**: An image file showing the dashboard with analysis results.
- **Uber_Rides_Data_Analysis_Documentation_and_Recommendations.docx**: A document detailing analysis steps and recommendations.

## Analysis Steps

### 1. Importing Libraries
- Used `pandas` for data manipulation, `numpy` for numerical operations, and `matplotlib.pyplot` & `seaborn` for data visualization.

### 2. Loading the Dataset
- Loaded the Uber dataset from a CSV file and displayed the first 10 rows to understand its structure.

### 3. Basic Data Exploration
- Generated summary statistics, checked for missing values, duplicate rows, and unique values in each column.

### 4. Handling Missing Values
- Used forward fill (`ffill`) for the 'PURPOSE' column.
- Filled missing values in 'Month' and 'Year' columns using the mode and converted them to integer type.

### 5. Converting Date Columns
- Converted 'START_DATE' and 'END_DATE' to datetime format.

### 6. Extracting Date and Time Components
- Extracted date, time, month, and year from 'START_DATE' and 'END_DATE' columns.
- Extracted hour and minute components from 'START_TIME' and 'END_TIME'.

### 7. Calculating Ride Duration
- Computed trip duration in minutes and added it as a new column.

### 8. Identifying Round Trips
- Created a new column `RTRIP` to identify round trips where `START*` and `STOP*` locations match.

### 9. Visualizing the Data
- Used Python visualizations (matplotlib & seaborn) to analyze ride distribution trends:
  - **Heatmaps** for correlation analysis
  - **Bar charts** for categorical data comparisons
  - **Line plots** for trends over time
  - **Histograms** for ride duration distribution

### 10. Saving Cleaned Data
- Saved the cleaned and processed dataset to `UberDatasetCleaned.csv`.

## Dashboard Insights

The dashboard includes the following visualizations:

1. **Number of Rides by Category**: Business vs. Personal rides.
2. **Number of Rides by Purpose**: Displays ride distribution across different purposes.
3. **Number of Rides and Total Miles by Month**: Trends in ride count and distance covered each month.
4. **Number of Rides by Day**: Ride distribution across weekdays.
5. **Average Miles Traveled by Weekday**: Analyzing travel distances for different days.
6. **Number of Rides by Month**: Seasonal trends in ride demand.

### Additional Insights from Python Visualizations
- **Total Miles Traveled per Category**: Comparison of miles traveled for business and personal rides.
- **Top 10 Pickup Locations**: Most frequent starting locations for rides.
- **Top 10 Drop Locations**: Common destinations for Uber rides.
- **Number of Round Trips**: Count of rides that started and ended at the same location.



