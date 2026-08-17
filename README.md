# Week 1 – Data Acquisition, Cleaning and Exploratory Data Analysis

## Project Overview

This project focuses on the data preparation and exploratory analysis process using a publicly available Student Performance and Learning Behavior dataset.

The main objective is to acquire the dataset, inspect its structure, clean the data, perform exploratory data analysis (EDA), create meaningful visualizations, and identify important patterns within the dataset using Python.

## Objectives

* Acquire a publicly available dataset.
* Understand the structure and characteristics of the dataset.
* Identify and handle missing values.
* Detect and remove duplicate records.
* Check and validate data types.
* Calculate descriptive statistics.
* Perform exploratory data analysis.
* Create meaningful data visualizations.
* Draw insights from the analysis.

## Dataset

**Dataset:** Student Performance and Learning Behavior Dataset

**Domain:** Education and Student Performance

**Original Records:** 14,003

**Number of Features:** 16

The dataset contains information related to students' study habits, attendance, motivation, learning behavior, educational resources, exam performance, and final grades.

### Main Features

* StudyHours
* Attendance
* Resources
* Extracurricular
* Motivation
* Internet
* Gender
* Age
* LearningStyle
* OnlineCourses
* Discussions
* AssignmentCompletion
* ExamScore
* EduTech
* StressLevel
* FinalGrade

## Tools and Technologies

* Python 3.14.6
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Visual Studio Code
* GitHub

## Data Cleaning

The original dataset was examined for missing values, duplicate records, and data types.

### Missing Values

No missing values were found in any of the 16 columns.

Therefore, no missing-value imputation was required.

### Duplicate Records

The dataset initially contained **1,534 duplicate records**.

These duplicate rows were removed using Pandas `drop_duplicates()`.

After cleaning:

* Original records: **14,003**
* Duplicate records removed: **1,534**
* Final cleaned records: **12,469**

### Data Types

All 16 columns were stored as integer (`int64`) data types.

Since the data types were appropriate for the numerical and encoded variables in the dataset, no data-type conversion was required.

## Exploratory Data Analysis

Descriptive statistics were calculated after removing duplicate records.

### Key Statistics

| Measure             | Result |
| ------------------- | -----: |
| Average Study Hours |  20.03 |
| Average Attendance  | 80.24% |
| Average Exam Score  |  70.31 |
| Median Exam Score   |     70 |
| Minimum Exam Score  |     40 |
| Maximum Exam Score  |    100 |

## Visualizations

### 1. Distribution of Exam Scores

This histogram shows how exam scores are distributed among the students. Scores are spread across the range of approximately 40 to 100, with students represented across different performance levels.

### 2. Study Hours vs Exam Score

The scatter plot compares students' study hours with their exam scores. It helps visually examine whether a relationship exists between the amount of study time and examination performance.

### 3. Correlation Heatmap

The correlation heatmap presents the relationships between the numerical variables in the dataset. It helps identify variables that have stronger or weaker linear relationships with one another.

### 4. Exam Score Box Plot

The box plot summarizes the distribution of exam scores and helps identify the central tendency, spread, and possible outliers.

## Key Insights

1. The cleaned dataset contains **12,469 records** after removing 1,534 duplicate records.

2. The average study time is approximately **20.03 hours**, while the average attendance is approximately **80.24%**.

3. The average exam score is **70.31**, with scores ranging from **40 to 100**.

4. The median exam score is **70**, indicating that the middle observation lies around the 70-mark level.

5. The correlation analysis shows very weak linear relationships between ExamScore and the selected variables:

   * AssignmentCompletion: **0.0274**
   * StudyHours: **0.0042**
   * Motivation: **−0.0035**
   * Attendance: **−0.0142**

6. The correlation values are close to zero, so these variables do not show a strong linear relationship with exam scores in this dataset.

## Project Files

* `Week1_EDA.py` – Python code used for data cleaning and exploratory analysis.
* `student_performance.csv` – Original dataset.
* `student_performance_cleaned.csv` – Dataset after duplicate removal.
* `exam_score_distribution.png` – Exam score distribution visualization.
* `study_hours_vs_exam_score.png` – Study hours versus exam score visualization.
* `correlation_heatmap.png` – Correlation heatmap.
* `exam_score_boxplot.png` – Exam score box plot.
* `README.md` – Project documentation.

## Conclusion

The Week 1 analysis demonstrated the major stages of data preparation and exploratory analysis. The dataset was inspected, checked for missing values and duplicate records, and validated for data types. A total of 1,534 duplicate records were removed, resulting in a cleaned dataset containing 12,469 records.

EDA was then performed using descriptive statistics and four visualizations. The analysis provided an overview of student study patterns and examination performance and demonstrated how Python libraries such as Pandas, Matplotlib, and Seaborn can be used for practical data analysis.

## Future Scope

Further analysis could investigate relationships between student characteristics, learning behavior, stress levels, educational resources, and final grades using statistical analysis or machine learning techniques.
