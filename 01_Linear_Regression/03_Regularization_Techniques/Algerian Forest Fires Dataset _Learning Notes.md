# Algerian Forest Fires Dataset - Learning Notes

## Overview

* Worked on the Algerian Forest Fires Dataset.
* Performed data cleaning, preprocessing, feature engineering, and exploratory data analysis (EDA).
* Analyzed fire and non-fire observations from two regions of Algeria.

## Data Cleaning

* Loaded the dataset using Pandas.
* Checked dataset structure using `head()`, `info()`, and `describe()`.
* Identified and handled missing values.
* Removed null and inconsistent rows.
* Renamed and cleaned column names using `str.strip()`.
* Created a new `Region` feature to distinguish between the two regions.
* Converted columns to appropriate data types (`int` and `float`).

## Feature Engineering

* Created a `Region` column:

  * 0 → Bejaia Region
  * 1 → Sidi-Bel Abbes Region
* Encoded the target variable (`Classes`):

  * Fire → 1
  * Not Fire → 0

## Data Preprocessing

* Removed unnecessary columns (`day`, `month`, `year`) for analysis.
* Saved the cleaned dataset into a new CSV file.

## Exploratory Data Analysis (EDA)

* Generated summary statistics using `describe()`.
* Checked class distribution using `value_counts()`.
* Created histograms to understand feature distributions.
* Used pie charts to visualize Fire vs Not Fire percentages.
* Calculated feature correlations using `corr()`.
* Visualized correlations using a heatmap.
* Used boxplots to identify outliers.

## Insights from Analysis

* August and September recorded the highest number of forest fires.
* Fire incidents were more frequent during summer months.
* Correlation analysis helped identify relationships among weather and fire-related features.
* Data visualization provided a better understanding of feature distributions and class balance.

## Libraries Used

* NumPy
* Pandas
* Matplotlib
* Seaborn

## Key Concepts Learned

* Data Cleaning
* Missing Value Handling
* Feature Engineering
* Label Encoding
* Data Type Conversion
* Exploratory Data Analysis (EDA)
* Correlation Analysis
* Heatmaps
* Histograms
* Boxplots
* Pie Charts
* Dataset Preparation for Machine Learning
