# 📊 Data Jobs Salary Dashboard | Microsoft Excel

![Salary Dashboard](/Resources/Images/1_Salary_Dashboard_Final_Dashboard.gif)

## 📖 Overview

This project analyzes the **2023 Data Jobs dataset** using Microsoft Excel to explore salary trends across different data-related careers. The dashboard enables users to interactively compare salaries based on **job title**, **country**, and **employment type**, helping uncover insights into the global data job market.

The objective of this project was to demonstrate how Excel can be used to clean data, perform analysis, build interactive dashboards, and communicate insights effectively.

---

## 📂 Dashboard File

The complete Excel dashboard is available here:

📄 **[1_Project_Dashboard.xlsx](1_Project_Dashboard.xlsx)**

---

## 🛠️ Skills Demonstrated

* 📊 Dashboard Design
* 📈 Pivot Tables & Pivot Charts
* 🧮 Advanced Excel Formulas
* 🎯 Data Validation
* 🗺️ Map Charts
* 📋 Data Analysis
* 📉 Data Visualization
* 📌 Interactive Reporting

---

## 📁 Dataset

The dashboard is built using a real-world **2023 Data Jobs** dataset containing information such as:

* 👨‍💼 Job Titles
* 💰 Average Salaries
* 🌍 Countries
* 🏢 Employment Types
* 🛠️ Required Skills

---

# Dashboard Walkthrough

## 📊 Salary Comparison by Job Title

<img src="/Resources/Images/1_Salary_Dashboard_Chart1.png" width="850" height="550" alt="Salary Dashboard Chart1">

### Excel Features Used

* Horizontal Bar Chart
* Number Formatting
* Dynamic Dashboard Layout

### Insights

* Senior-level roles generally command the highest salaries.
* Data Engineers and Data Scientists tend to earn more than Analyst positions.
* Sorting salaries in descending order makes comparisons intuitive and easy to interpret.

---

## 🌍 Median Salary by Country

![Country Map](/Resources/Images/1_Salary_Dashboard_Country_Map.gif)

### Excel Features Used

* Map Chart
* Conditional Formatting
* Geographic Data Visualization

### Insights

* Salary levels vary significantly across countries.
* The map provides an easy way to compare global salary trends.
* High-paying and lower-paying regions can be identified at a glance.

---

# Advanced Excel Techniques

## 🧮 Dynamic Median Salary Calculation

```excel
=MEDIAN(
IF(
(jobs[job_title_short]=A2)*
(jobs[job_country]=country)*
(ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
(jobs[salary_year_avg]<>0),
jobs[salary_year_avg]
)
)
```

### Purpose

This formula dynamically calculates the **median salary** based on multiple criteria:

* Job Title
* Country
* Employment Type

It powers the dashboard by returning salary values based on the user's selected filters.

### Background Table

![Background Table](/Resources/Images/1_Salary_Dashboard_Screenshot1.png)

### Dashboard Implementation

<img src="/Resources/Images/1_Salary_Dashboard_Job_Title.png" width="400" height="500" alt="Salary Dashboard Title">

---

## 🔎 Dynamic Filter List

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

### Purpose

This formula creates a clean list of employment types by removing unnecessary values before they are used in dashboard filters.

### Background Table

![Background Table](/Resources/Images/1_Salary_Dashboard_Screenshot2.png)

### Dashboard Implementation

<img src="/Resources/Images/1_Salary_Dashboard_Type.png" width="350" height="500" alt="Salary Dashboard Type">

---

# 🎯 Interactive Dashboard

## ❎ Data Validation

<img src="/Resources/Images/1_Salary_Dashboard_Data_Validation.gif" width="425" height="400" alt="Salary Dashboard Data Validation">

Dropdown menus were created using **Data Validation**, allowing users to filter the dashboard by:

* Job Title
* Country
* Employment Type

This improves usability by ensuring consistent input while making the dashboard fully interactive.

---

# 📌 Key Insights

* Senior Data Professionals generally earn the highest salaries.
* Salary varies considerably depending on country.
* Employment type can influence compensation.
* Interactive filtering makes it easy to explore salary trends across different job markets.

---

# 🚀 What I Learned

Through this project, I strengthened my skills in:

* Building interactive Excel dashboards
* Working with real-world datasets
* Writing advanced Excel formulas
* Designing clear and informative visualizations
* Presenting business insights through data

---

# 🔮 Future Improvements

* Automate data preparation using Power Query.
* Expand the dashboard with additional KPIs.
* Rebuild the dashboard in Power BI for enhanced interactivity.
* Connect the dashboard to live datasets for automatic updates.

---

## ⭐ If you found this project helpful, consider giving it a star!
