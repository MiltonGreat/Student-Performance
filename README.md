# Student Performance Analysis

### Overview

This project focuses on analyzing student performance data to understand key patterns, correlations, and outliers. The dataset contains information about students from two Portuguese schools and their academic achievements in math and Portuguese classes. The project includes data cleaning, visualization, and statistical analysis.

### Dataset

The dataset includes two CSV files:

- student-mat.csv: Data related to students enrolled in a Math course.
- student-por.csv: Data related to students enrolled in a Portuguese language course.

Both datasets share several columns, including demographic information and academic performance (grades).

The dataset contains the following information:

- Demographic Information: Gender, age, address, family size, etc.
- Educational Background: Mother's and father's education levels, type of school, etc.
- Behavioral and Academic Data: Weekly study time, alcohol consumption, family relationships, grades (G1, G2, G3), etc.

### Steps in Project

This project performs the following steps:

1. Data Loading
- Reads the student-mat.csv and student-por.csv files into pandas DataFrames.
- Displays the first few rows to confirm successful loading.

2. Missing Data Handling
- Checks for missing values in both datasets.
- Imputes missing numerical data using the mean and categorical data using the most frequent value.

3. Outlier Detection and Removal
- Visualizes outliers using boxplots.
- Removes outliers based on the interquartile range (IQR) method.

4. Data Normalization
- Normalizes numeric columns using StandardScaler from scikit-learn.

5. Dataset Merging
- Merges the math and Portuguese datasets using shared columns such as school, sex, and age.

6. Data Visualization
- Creates visualizations to identify trends, distributions, and correlations:
    - Distribution of student ages.
    - Boxplots for numerical features.
    - Correlation heatmap for numeric columns.
    - Grade distribution for G1, G2, and G3.
    - Study time vs. final grade (G3).

7. Data Export
- Saves the cleaned datasets to student-mat-cleaned.csv and student-por-cleaned.csv.

### Key Insights

- The analysis provides insights into factors influencing student performance, such as study time, attendance, and socio-economic factors.
- The visualizations highlight the impact of study time on final grades and the distribution of grades across students.

### Future Enhancements

- Extend the analysis to include predictive modeling for student performance.
- Explore additional correlations, such as the effect of parental education levels on grades.
- Develop an interactive dashboard for visualizing student performance.

### Source

Dataset: [Student Performance Dataset on Kaggle](https://www.kaggle.com/datasets/impapan/student-performance-data-set)
