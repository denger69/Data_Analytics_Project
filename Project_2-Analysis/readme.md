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

<img width="1788" height="1264" alt="image" src="https://github.com/user-attachments/assets/99e2f5a8-9fc8-4189-bb6f-9368f5b5b8f9" />

📃 **Power Pivot Menu Tools:**  

Refined the model and created DAX measures with ease  

<img width="1918" height="742" alt="image" src="https://github.com/user-attachments/assets/e93613cb-211c-4493-bf25-fee7de57aaba" />


📊 **Analysis & Insights**  

💻 **Dominant Tools:**  

- **SQL** and **Python** emerged as top skills in job listings

- These skills play a foundational role in most data workflows

☁️ **Emerging Technologies:**  

- Cloud platforms like **AWS** and **Azure** show rising demand  
- Reflects shift toward big data and scalable infrastructure

<img width="759" height="513" alt="image" src="https://github.com/user-attachments/assets/acc23247-7afd-4009-901f-8fcb50c51834" />


🤔 **So What?**  
Identifying dominant and emerging skills helps:
- Professionals stay competitive in evolving job markets  
- Educators focus curriculum on high-impact tools

# 4️⃣ What’s the Pay of the Top 10 Skills?

📊 **Skill Focus:** Advanced Charts (PivotChart)  

📈 **Visualization Technique:**  

Used a **Combo PivotChart** to explore how skill demand correlates with median salary:

- 🪙 **Primary Axis:** Median Salary (Clustered Column)
  
- 👍 **Secondary Axis:** Skill Likelihood (%) (Line with Diamond Markers)

🎨 **Chart Customizations:**

- Added axis titles for clarity
  
- Removed line connectors for skill likelihood
  
- Changed markers to **diamonds** for visual distinction

<img width="862" height="452" alt="image" src="https://github.com/user-attachments/assets/8594bc42-00c3-4624-9178-6724b389cc5c" />


📊 **Analysis & Insights:**

💰 **High-Paying Skills:**

- **Python**, **Oracle**, and **SQL** are linked to higher median salaries
  
- Indicate strong market value and technical depth

📉 **Low-Paying Skills:**

- **PowerPoint** and **Word** show lowest salary and likelihood
  
- Suggest lower specialization and less relevance in data-focused roles

🤔 **So What?**
- Investing in in-demand skills like **Python** and **SQL** can significantly enhance earning potential  
- Especially valuable for professionals aiming for high-paying roles in tech and analytics

# 🧾 Conclusion

This project offered a deep dive into the data science job market using Excel as a powerful analytics platform. Through skills like **Power Query**, **PivotTables**, **Power Pivot**, **DAX**, and **Advanced Charts**, I explored how job roles, skills, and geography influence salary dynamics. Key findings reveal that **technical depth** (e.g. Python, SQL, Oracle) and **cloud expertise** (AWS, Azure) correlate strongly with higher pay, while broader skills like Word or PowerPoint command less market value.

Understanding these patterns equips professionals to make informed career decisions and helps educators prioritize training in high-impact skills. Excel proved more than capable as a tool for surfacing insights, telling a story, and guiding strategy—one PivotTable at a time.

