# Student Performance Analysis

### Overview

This project focuses on analyzing student performance data to uncover key patterns, correlations, and outliers. The dataset contains information about students from two Portuguese schools, including their academic achievements in math and Portuguese courses. The project involves data cleaning, exploratory data analysis (EDA), and statistical analysis, aimed at understanding factors that influence student performance.

### EDA Questions

I want to answer the following questions:

1. What is the distribution of student ages?
2. How do student grades (G1, G2, G3) distribute across the dataset?
3. What is the relationship between study time and final grade (G3)?
4. Is there a significant difference in final grades across different study times?
5. How does gender affect final grades (G3) in relation to study time?
6. What is the correlation between different numerical features (e.g., grades, study time, family background)?
7. What is the quality of family relationships and its impact on students' performance
8. How do alcohol consumption patterns affect academic performance?
9. What is the impact of the number of past class failures on final grades (G3)?

### Dataset

The dataset includes two CSV files:

- student-mat.csv: Data related to students enrolled in a Math course.
- student-por.csv: Data related to students enrolled in a Portuguese language course.

Both datasets share several columns, including demographic information and academic performance (grades).

The dataset contains the following information:

- **Demographic Information**: Gender, age, address, family size, etc.
- **Educational Background**: Mother's and father's education levels, type of school, etc.
- **Behavioral and Academic Data**: Weekly study time, alcohol consumption, family relationships, grades (G1, G2, G3), etc.

### Steps in Project

This project performs the following steps:

1. **Data Loading**
- Reads the student-mat.csv and student-por.csv files into pandas DataFrames.
- Displays the first few rows to confirm successful loading.

2. **Missing Data Handling**
- Checks for missing values in both datasets.
- Imputes missing numerical data using the mean and categorical data using the most frequent value.

3. **Outlier Detection and Removal**
- Visualizes outliers using boxplots.
- Removes outliers based on the interquartile range (IQR) method.

4. **Data Normalization**
- Normalizes numeric columns using StandardScaler from scikit-learn.

5. **Dataset Merging**
- Merges the math and Portuguese datasets using shared columns such as school, sex, and age.

6. **Data Visualization**
- Distribution of student ages: Visualizes the age distribution across students.
- Grade distribution (G1, G2, G3): Analyzes the distribution of student grades across different stages.
- Study time vs. final grade (G3): Investigates the relationship between study time and final grades using boxplots.
- ANOVA test for study time: Checks if there is a significant difference in final grades across different study times.
- Gender comparison: Explores how gender affects final grades in relation to study time.
- Correlation heatmap: Shows correlations between numeric features such as grades, study time, and family relationships.
- Family relationship quality vs. final grade: Examines how family relationship quality impacts academic performance.
- Alcohol consumption vs. final grade: Analyzes the effect of alcohol consumption on academic performance.
- Past failures vs. final grade: Investigates the impact of previous failures on final grades.
- 
### Key Insights

## Conclusion

1. **Age Distribution**: Both datasets exhibit similar age distributions, with students generally ranging from 15 to 20 years, and an average age around 16.4. This suggests that age is not a significant differentiator between the two datasets.

2. **Family Education**: The average family education scores (Medu and Fedu) are slightly higher in the student-mat dataset compared to the student-por dataset, suggesting a slight difference in parental education levels across the two groups. However, this difference is relatively minor.

3. **Travel Time**: Both datasets show similar travel times, with an average of around 1.34 for student-mat and 1.45 for student-por. This indicates that the students in both datasets have similar commute times to school, with no significant outliers observed.
    
4. **Study Time**: The average study time in both datasets is about 2 hours, with minimal variation between them. While there is some diversity in study habits (with a standard deviation of 0.69 vs. 0.70), the overall study time appears consistent between the two groups.

5. **Failures**: No failures were reported in either dataset after outlier removal, indicating that students in both groups performed well academically during the observed periods.

6. **Family Relationships and Free Time**: Both datasets exhibit positive family relationships (average score around 4), suggesting strong support systems at home. Similarly, students report having moderate levels of free time, with both datasets showing similar results.

7. **Health**: Both groups report healthy student populations, with average health scores of approximately 3.52 in student-mat and 3.59 in student-por, indicating that health factors are unlikely to significantly impact academic performance.

8. **Absences**: The student-mat dataset reports higher average absences (4.05) compared to the student-por dataset (2.77). This suggests that students in student-mat missed more school days on average, which could have implications for academic performance, although further investigation is needed to determine the reasons behind these absences.

9. **Grades**: The average grades (G1, G2, G3) are slightly lower in the student-mat dataset compared to the student-por dataset, with the distribution of grades being fairly similar. The presence of a 0 grade in G3 for student-mat indicates that some students may have failed, although these students were likely removed due to being considered outliers.

10. **Correlations**: The analysis found weak correlations between study time and grades (G1, G2, G3), with a slight negative correlation with failures. This suggests that students who study more tend to have fewer academic failures, although the correlation is not strong. Additionally, family relationships (famrel) show a weak positive correlation with free time, indicating that students with stronger family relationships may enjoy slightly more free time.

### Source

Dataset: [Student Performance Dataset on Kaggle](https://www.kaggle.com/datasets/impapan/student-performance-data-set)
