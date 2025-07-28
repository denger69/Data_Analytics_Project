# Excel Data Analytics: Insights into Data Science Careers

## Introduction

As a former job seeker, I’ve often been struck by the lack of data analyzing the best jobs and skills in the data science market. This inspired me to explore which skills top employers prioritize and how to secure higher pay.

## To analyze the data science job market, I considered the following questions:

**- Do additional skills lead to higher pay?**

**- What are the salary ranges for data jobs in various regions?**

**- Which skills are most valued among data professionals?**

**- How much do the top 10 skills earn on average?**

## 🔧 Excel Skills Used

**The following Excel skills were utilized for analysis:**

**🧭 Pivot Tables** – To explore data from different angles with dynamic summaries

**📊 Pivot Charts**– For visual storytelling through charted insights

**🧠 DAX (Data Analysis Expressions**) – Crafting powerful measures for deeper analysis

**🧼 Power Query** – Streamlining data cleaning and transformations

**🧩 Power Pivot** – Integrating data models with calculated relationships

## Data Jobs Dataset

The dataset used for this project consists of real-world data science job information from 2023, including detailed information on job titles, salaries, locations, and skills.

**It includes detailed information on:**

👨‍💼 Job titles
💰 Salaries
📍 Locations
🛠️ Skills

# 1️⃣ Do more skills get you better pay

## 🔍 Skill: Power Query (ETL)

### **Extract**

I first used Power Query to extract the original data (data_salary_all.xlsx) and create two queries:

🗃️ First one with all the data jobs information.

🔧 The second listing the skills for each job ID.

### **Transform**

I transformed each query by adjusting column types, removing irrelevant columns, cleaning text to remove specific words, and trimming extra whitespace.

**📊 data_jobs_all**

<img width="244" height="312" alt="image" src="https://github.com/user-attachments/assets/11e7fd1d-a64e-4d5c-9392-fc4e9da17868" />

**🛠️ data_job_skills**

<img width="243" height="328" alt="image" src="https://github.com/user-attachments/assets/1f3d4984-1ae6-4e09-9bf5-2b5fab630535" />

### **🔗 Load**

Finally, I imported both transformed queries into the workbook, laying the groundwork for my upcoming analysis.

**📊 data_jobs_all**

<img width="1916" height="649" alt="image" src="https://github.com/user-attachments/assets/61a91730-e1d4-4504-b177-e4a36d4422c3" />



**🛠️ data_job_skills**

<img width="1914" height="702" alt="image" src="https://github.com/user-attachments/assets/26d3d5e1-0cf9-4ff1-8690-7e2f117e9c72" />

## 📊 Analysis

### 💡 Insights

📈 There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like **Senior Data Engineer** and **Data Scientist**.

💼 Roles that require fewer skills, such as **Business Analyst**, tend to offer lower salaries—suggesting that more specialized skill sets command higher market value.

<img width="874" height="537" alt="image" src="https://github.com/user-attachments/assets/237efc6c-2977-45c9-8b31-be670b8c357d" />

### 🧠 So What?

This trend reinforces the importance of continuously expanding your skill set—especially if you're aiming for roles with higher compensation and influence in the data space.

# 2️⃣ What’s the salary for data jobs in different regions?

## 🧮 Skills: PivotTables & DAX

## 📈 Pivot Table Analysis

🔢 **PivotTable Creation:**  
Built using the Data Model from **Power Pivot** to enable deeper analysis.

📊 **Configuration:**  
- **Rows Area:** `job_title_short`  
- **Values Area:** `salary_year_avg`

🧮 **Calculated Measure for India:**  
Used DAX to compute the median salary for jobs located in India:

DAX

=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "India"
)

**🧠 DAX Formula for Overall Median Salary:**

Median Salary := MEDIAN(data_jobs_all[salary_year_avg])

# 3️⃣ What Are the Top Skills of Data Professionals?

🔧 **Skill Spotlight:** Power Pivot  

💪 **Why Power Pivot Matters:**  

Enabled creation of a unified data model by integrating `data_jobs_all` and `data_jobs_skills`.

🔗 **Data Model Construction:**  

- Used **Power Query** for initial data cleaning
  
- Established relationships between tables using `job_id` as the key
  
- Power Pivot automatically connected the tables for efficient analysis

📃 **Power Pivot Menu Tools:**  

Refined the model and created DAX measures with ease  



📊 **Analysis & Insights**  

💻 **Dominant Tools:**  

- **SQL** and **Python** emerged as top skills in job listings

- These skills play a foundational role in most data workflows

☁️ **Emerging Technologies:**  

- Cloud platforms like **AWS** and **Azure** show rising demand  
- Reflects shift toward big data and scalable infrastructure

![Skill Analysis Chart](2_Project_Analysis_Chart3.png)

🤔 **So What?**  
Identifying dominant and emerging skills helps:
- Professionals stay competitive in evolving job markets  
- Educators focus curriculum on high-impact tools

