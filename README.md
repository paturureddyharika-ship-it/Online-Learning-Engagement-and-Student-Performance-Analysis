# 📊 Online Education Analytics Dashboard

 📌 Project Overview

This project analyzes **online education data** to understand student performance, engagement, dropout patterns, risk levels, and regional trends.

The project uses **SQL for data analysis and querying** and **Microsoft Power BI for interactive data visualization and dashboard creation**.

The main goal is to transform raw online education data into meaningful insights that can help understand student learning behavior and academic outcomes.

---

## 🎯 Project Objectives

* Analyze overall student performance.
* Measure student engagement levels.
* Identify student dropout patterns.
* Analyze student risk levels.
* Compare performance across different regions.
* Understand the relationship between student engagement and academic performance.
* Analyze the relationship between total clicks and student performance.
* Compare students based on their highest education level.
* Create an interactive Power BI dashboard for data visualization.

---

## 🛠️ Tools & Technologies

| Tool                  | Purpose                                   |
| --------------------- | ----------------------------------------- |
| 🗄️ MySQL             | Data analysis and SQL queries             |
| 📊 Microsoft Power BI | Dashboard and visualization               |
| 📁 CSV                | Dataset                                   |
| 💻 SQL                | Data querying and analysis                |
| 📈 DAX                | Power BI calculations and measures        |
| 📝 GitHub             | Project documentation and version control |

---

## 📂 Project Files

```text
Online-Education-Analytics/
│
├── 📊 Powerbi(1).pbix
├── 🗄️ sql data.sql
├── 📁 online_education_dataset.csv
└── 📖 README.md
```

### File Description

**Powerbi(1).pbix**
Power BI project file containing the interactive dashboard, visualizations, data model, and analysis.

**sql data.sql**
SQL script containing queries used to analyze the online education dataset.

**online_education_dataset.csv**
Raw dataset containing online education/student-related data used for analysis.

---

## 🗄️ SQL Analysis

The SQL analysis includes queries for:

### 👨‍🎓 Student Count

Calculates the total number of unique students.

```sql
SELECT COUNT(DISTINCT id_student) AS total_students
FROM online_education_dataset;
```

### 📊 Average Student Score

Calculates the average student score.

```sql
SELECT ROUND(AVG(avg_score), 2) AS average_student_score
FROM online_education_dataset;
```

### 🖱️ Average Student Engagement

Analyzes the average number of clicks made by students.

```sql
SELECT ROUND(AVG(total_clicks), 2) AS average_total_clicks
FROM online_education_dataset;
 🎓 Pass & Dropout Analysis

Calculates the number of students who passed and dropped out.

```sql
SELECT
    SUM(CASE WHEN pass_flag = 1 THEN 1 ELSE 0 END) AS students_passed,
    SUM(CASE WHEN dropout_flag = 1 THEN 1 ELSE 0 END) AS students_dropped_out
FROM online_education_dataset;
```

### 📈 Engagement Level Analysis

Analyzes the number of students in each engagement category.

```sql
SELECT
    engagement_level,
    COUNT(DISTINCT id_student) AS total_students
FROM online_education_dataset
GROUP BY engagement_level
ORDER BY total_students DESC;
```

### ⚠️ Risk Level Analysis

Analyzes students according to their risk level.

```sql
SELECT
    risk_level,
    COUNT(DISTINCT id_student) AS total_students
FROM online_education_dataset
GROUP BY risk_level
ORDER BY total_students DESC;
```

### 📚 Performance Analysis

Compares student performance levels and average scores.

```sql
SELECT
    performance_level,
    COUNT(DISTINCT id_student) AS total_students,
    ROUND(AVG(avg_score), 2) AS average_score
FROM online_education_dataset
GROUP BY performance_level
ORDER BY average_score DESC;
```

### 🌍 Regional Analysis

Analyzes student count, average score, and average clicks by region.

```sql
SELECT
    region,
    COUNT(DISTINCT id_student) AS total_students,
    ROUND(AVG(avg_score), 2) AS average_score,
    ROUND(AVG(total_clicks), 2) AS average_clicks
FROM online_education_dataset
GROUP BY region
ORDER BY total_students DESC;
```

---

## 📊 Power BI Dashboard

The Power BI dashboard provides interactive visualizations for exploring:

* Total Students
* Student Performance
* Engagement Levels
* Dropout Analysis
* Risk Levels
* Average Student Score
* Average Total Clicks
* Regional Analysis
* Education Level Analysis
* Click/Engagement Patterns

Users can interact with the dashboard using filters and visual elements to explore different aspects of the dataset.

---

## 🔍 Key Analysis Areas

### 1. Student Engagement

The project analyzes different engagement levels and compares them with student performance.

### 2. Student Performance

Student performance is analyzed using average scores and performance categories.

### 3. Dropout Analysis

Dropout rates are analyzed based on:

* Engagement level
* Performance level
* Other student characteristics

### 4. Risk Analysis

Students are grouped according to risk levels to understand potential academic concerns.

### 5. Regional Analysis

Student count, average score, and average clicks are compared across different regions.

### 6. Education Level Analysis

The project analyzes student performance and engagement based on their highest education level.

---

## 📈 Dashboard Insights

The dashboard is designed to help users identify:

* Differences in student engagement.
* Patterns in student performance.
* Dropout trends.
* High-risk student groups.
* Regional differences.
* Relationship between student activity and academic performance.

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
CSV Data
     ↓
MySQL Database
     ↓
SQL Queries & Analysis
     ↓
Power BI
     ↓
DAX Measures
     ↓
Interactive Dashboard
     ↓
Insights & Visualization
```

---

## 💡 Skills Demonstrated

* SQL
* MySQL
* Data Cleaning
* Data Analysis
* Power BI
* DAX
* Data Visualization
* Dashboard Development
* Exploratory Data Analysis
* Business Intelligence
* Git & GitHub

---

## 🚀 How to Use This Project

### Step 1 – Download the Repository

Clone or download this repository from GitHub.

### Step 2 – Import the Dataset

Import:

```text
online_education_dataset.csv
```

into MySQL.

### Step 3 – Run SQL Queries

Open:

```text
sql data.sql
```

and execute the queries in MySQL.

### Step 4 – Open Power BI

Open:

```text
Powerbi(1).pbix
```

using Microsoft Power BI Desktop.

### Step 5 – Explore the Dashboard

Use the available filters and visualizations to analyze student performance, engagement, dropout, risk, and regional patterns.

---

## 📸 Dashboard Screenshots

Add your Power BI dashboard screenshots here:

```markdown
![Power BI Dashboard](screenshots/dashboard.png)
```

You can create a folder:

```text
screenshots/
```

and add your dashboard images there.


📌 Conclusion

This project demonstrates how **SQL and Power BI can be combined to analyze online education data**. SQL is used to extract and analyze meaningful information from the dataset, while Power BI transforms the results into interactive and easy-to-understand visualizations.

The project provides a practical example of a **Data Analytics / Business Intelligence workflow**, from raw data to analysis and visualization.


## 👩‍💻 Author

**Harika**

Data Analytics | SQL | Power BI | DAX

---

⭐ If you find this project useful, feel free to explore the repository and learn from the analysis.
