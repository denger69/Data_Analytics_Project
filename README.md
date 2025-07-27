# Data_Analytics_Project
My first Excel dashboard project showcasing data science salary trends, built using advanced Excel techniques like dynamic charts, PivotTables, slicers, and structured formulas to explore skill correlations and job insights.

#**Salary Dashboard**
<img width="1347" height="619" alt="1_Salary_Dashboard" src="https://github.com/user-attachments/assets/45eb1411-c65c-4a06-81c8-478528e62dd3" />

**Introduction**
This salary dashboard for data jobs helps job seekers explore salaries for their preferred roles and secure fair compensation. It offers detailed insights into job titles, salaries, locations, and essential skills, all displayed in a clear and user-friendly format.

**Dashboard File**
(Project_1-Dashboard/Salary_Distribution.xlsx)

**Excel skills used for the analysis include charts, formulas and functions, data validation, and conditional formatting.**

**Data Jobs Dataset**

The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

👨‍💼 Job titles

💰 Salaries

📍 Locations

🛠️ Skills

**📊 Dashboard Build Overview**
**1. Charts**

**📉 Data Science Job Salaries – Bar Chart**

**Excel Features:** Bar chart with formatted salary values and optimized layout

**Design Choice:** Horizontal orientation for intuitive median salary comparison

**Data Organization:** Job titles sorted by descending salary

**Insights Gained:** Senior roles and Engineers tend to earn more than Analyst roles

**🗺️ Country Median Salaries – Map Chart**

**Excel Features:** Excel’s map chart for global salary visualization

**Design Choice:** Color-coded regions by salary level

**Data Representation:** Median salary plotted per country

**Visual Enhancement:** Immediate understanding of geographic disparities

**Insights Gained:** Highlights high/low salary regions around the world

**2. Formulas & Functions**

**💰 Median Salary by Job Titles**

**=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))* 
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
**

**Multi-Criteria Filtering:** Matches job title, country, schedule type; excludes zero salaries

**Array Formula:** Combines MEDIAN() and nested IF() logic for dynamic insight

**Purpose:** Returns salary insights tailored by region, title, and job type

**3. Job Schedule Type Filter**

**Unique List Generation:** Filters out compound and empty values

**Purpose:** Populates background table with unique job schedule types
**4. Enhanced Data Validation**

**Filtered List Implementation:** Applied via Data Validation for Job Title, Country, and Type

**Benefits:**

✅ Restricts inputs to valid schedule types

🚫 Prevents inconsistent entries

👥 Improves dashboard usability

**Conclusion**

This dashboard offers a clear, interactive view of salary trends across job roles and countries. By blending charts, smart formulas, and validation, it makes complex insights accessible—helping users quickly identify high-paying roles and regions while exploring how schedule type impacts compensation.
