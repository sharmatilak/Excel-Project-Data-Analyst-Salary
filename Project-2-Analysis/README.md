# 📊 Data Jobs Market Analysis | Microsoft Excel

## 📖 Overview

This project explores a real-world **2023 Data Jobs** dataset to uncover trends in salaries, in-demand skills, and hiring patterns across the data industry.

Using Microsoft Excel, I performed data cleaning, transformation, modeling, and analysis with **Power Query, Power Pivot, Pivot Tables, DAX, and interactive charts** to answer key business questions and present actionable insights.

---

## 🎯 Business Questions

This analysis answers the following questions:

1. **Do jobs requiring more skills offer higher salaries?**
2. **How do salaries vary across different regions?**
3. **Which technical skills are most in demand?**
4. **Which skills are associated with the highest salaries?**

---

## 🛠️ Skills Demonstrated

* 📥 Power Query (ETL)
* 📊 Pivot Tables
* 📈 Pivot Charts
* 🧮 DAX (Data Analysis Expressions)
* 💪 Power Pivot
* 📉 Data Visualization
* 📋 Data Modeling
* 🔍 Data Analysis

---

## 📁 Dataset

The project uses a real-world **2023 Data Jobs** dataset containing information such as:

* 👨‍💼 Job Titles
* 💰 Annual Salaries
* 🌍 Countries
* 🛠️ Required Skills
* 🏢 Employment Types

---

# 1️⃣ Do More Skills Lead to Higher Salaries?

## 📥 Power Query (ETL)

### Extract

The raw dataset was imported into **Power Query** and split into two tables:

* **data_jobs_all** – Job posting information
* **data_job_skills** – Skills associated with each job posting

### Transform

The data was cleaned and prepared by:

* Changing column data types
* Removing unnecessary columns
* Cleaning text values
* Trimming whitespace
* Preparing the data for analysis

**📊 data_jobs_all**

![2\_Project\_Analysis\_Screenshot1.png](/Resources/Images/2_Project_Analysis_Screenshot1.png)

**🛠️ data_job_skills**

![2\_Project\_Analysis\_Screenshot2.png](/Resources/Images/2_Project_Analysis_Screenshot2.png)

### Load

Both cleaned datasets were loaded into Excel's Data Model for further analysis.

**📊 data_jobs_all**

![2\_Project\_Analysis\_Screenshot3.png](/Resources/Images/2_Project_Analysis_Screenshot3.png)

**🛠️ data_job_skills**

![2\_Project\_Analysis\_Screenshot4.png](/Resources/Images/2_Project_Analysis_Screenshot4.png)

---

## 📊 Analysis

### 💡 Key Insights

* Roles requiring a wider range of technical skills generally offer higher salaries.
* Senior Data Engineers and Data Scientists combine both high salaries and extensive technical skill requirements.
* Business Analyst roles tend to require fewer technical skills and have comparatively lower salaries.

![2\_Project\_Analysis\_Chart1.png](/Resources/Images/2_Project_Analysis_Chart1.png)

### 📌 Takeaway

Developing multiple technical skills can significantly improve opportunities for higher-paying data careers.

---

# 2️⃣ Salary Comparison Across Regions

## 🧮 Pivot Tables & DAX

I used **Pivot Tables** with Excel's Data Model and created DAX measures to calculate median salaries across different regions.

### Regional Median Salary

```DAX
=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country]="United States"
)
```

### Median Salary Measure

```DAX
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```

---

## 📊 Analysis

### 💡 Key Insights

* Senior Data Engineers and Data Scientists consistently rank among the highest-paid roles.
* Salaries in the United States are generally higher than those in many other regions.
* Geographic location plays a major role in salary differences.

![2\_Project\_Analysis\_Chart2.png](/Resources/Images/2_Project_Analysis_Chart2.png)

### 📌 Takeaway

Understanding regional salary trends helps professionals make informed career and relocation decisions.

---

# 3️⃣ Most In-Demand Skills

## 💪 Power Pivot

I created a relational data model by connecting the job postings and skills datasets through the **job_id** field.

### Data Model

![2\_Project\_Analysis\_Screenshot5.png](/Resources/Images/2_Project_Analysis_Screenshot5.png)

### Power Pivot

Power Pivot was used to manage relationships and create reusable measures for analysis.

![2\_Project\_Analysis\_Screenshot6.png](/Resources/Images/2_Project_Analysis_Screenshot6.png)

---

## 📊 Analysis

### 💡 Key Insights

* SQL and Python are the most frequently requested technical skills.
* Cloud technologies such as AWS and Azure continue to grow in demand.
* Employers prioritize strong programming and database knowledge across data roles.

![2\_Project\_Analysis\_Chart3.png](/Resources/Images/2_Project_Analysis_Chart3.png)

### 📌 Takeaway

Mastering SQL and Python provides an excellent foundation for building a career in data analytics.

---

# 4️⃣ Which Skills Offer the Highest Salaries?

## 📈 Pivot Chart

A combination Pivot Chart was created to compare:

* 💰 Median Salary
* 📊 Skill Demand (%)

The visualization makes it easy to compare earning potential alongside market demand.

---

## 📊 Analysis

### 💡 Key Insights

* Python, SQL, and Oracle are associated with some of the highest median salaries.
* General productivity tools such as Microsoft Word and PowerPoint appear less frequently in high-paying technical roles.
* Specialized technical skills continue to command higher salaries.

![2\_Project\_Analysis\_Chart4.png](/Resources/Images/2_Project_Analysis_Chart4.png)

### 📌 Takeaway

Investing in high-demand technical skills can significantly increase long-term earning potential.

---

# 📌 Conclusion

This project demonstrates how Microsoft Excel can be used for an end-to-end data analytics workflow—from data extraction and transformation to modeling, visualization, and business insight generation.

By leveraging **Power Query**, **Power Pivot**, **DAX**, **Pivot Tables**, and **interactive charts**, I analyzed real-world job market data to identify salary trends, skill demand, and regional differences. The findings highlight the growing importance of technical skills such as SQL, Python, and cloud technologies while showcasing how Excel can be used to solve real business problems through data analysis.
