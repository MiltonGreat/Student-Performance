# Student Performance Data Cleaning Project

### Overview

This project demonstrates various data cleaning techniques using Python (Pandas and NumPy) to process a dataset of students' performance on standardized tests. The dataset includes information about students' grades, demographic data, and study-related behaviors. The primary goal of this project is to prepare the data for analysis by handling missing values, smoothing noisy data, and removing outliers.

### Quality Issues:

- Missing values for student demographics or study time.
- Outliers in test scores or study hours.
- Non-numeric data (e.g., family support) requiring encoding.

Cleaning/Transformation:
- Impute missing values using median or mode for categorical variables.
- Transform test scores into standardized z-scores for comparability.
- Encode categorical variables like "family support" using one-hot encoding.

Known Limitations:
- Self-reported data may introduce bias (e.g., study hours).
- Limited to a single region or school system, reducing generalizability.

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

- Data Inspection: Load and inspect the data for initial analysis.
- Handling Missing Values: Clean the dataset by either dropping rows with missing values or imputing them using suitable methods.
- Outlier Detection and Removal: Use boxplots and statistical methods (like IQR) to detect and remove outliers.
- Smoothing Noisy Data: Apply techniques such as rolling means to smooth data where necessary.
- Data Normalization: Normalize the data using techniques like StandardScaler to standardize numerical features.
- Data Merging: Merge the dataset if required, such as combining data from different courses (Math and Portuguese).
- Visualization: Use data visualization tools like matplotlib and seaborn to visualize various aspects of the dataset, including categorical and numerical distributions.
- Export Cleaned Data: Save the cleaned data into new CSV files for future analysis or model building.

### Source

https://www.kaggle.com/datasets/impapan/student-performance-data-set

