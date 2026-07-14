# Data-Analytics
Projects for Data Analytics role

## Excel
1. Salary Dashboard
2. Database Analysis

## Power BI
3. Mobile Sales Dashboard
   
# 1. Salary Dashboard

An interactive Excel dashboard analyzing 32,000+ global job postings in data-related roles (Data Analyst, Data Scientist, Data Engineer, etc.).

## Features
- Interactive filters for Job Title, Country, and Employment Type
- Salary insights (yearly/hourly) across roles, locations, and platforms
- Breakdown by job posting source (Indeed, LinkedIn, ZipRecruiter, etc.)
- Remote work, degree requirement, and health insurance flags
- Skills analysis extracted from job listings (SQL, Python, AWS, Tableau, Power BI, etc.)

## File Structure
- `Data` – Raw dataset
- `Salary_Dashboard` – Main interactive dashboard
- `Data Validation` – Lookup/validation lists
- `Jobs`, `Country`, `Type`, `Platform` – Reference tables

## Tech
Built entirely in Microsoft Excel using PivotTables, slicers, and data validation.

## Use Case
Explore salary trends and in-demand skills in the data job market — useful for job seekers, recruiters, and analysts.


# 2. Database Analysis: Salaries & Skills
 
Analysis of salary trends and in-demand skills across data and tech roles (Data Scientist, Data Engineer, Data Analyst, Software Engineer, Cloud Engineer, ML Engineer, Business Analyst, and more), built with Excel pivot tables and charts.
 
## 📁 Contents
 
```
Project_Analysis.xlsx
├── Salary_Vs_Skills        # Median salary vs. avg. skills required per job title
├── Salary_Analysis         # Median salary by job title, US vs. Non-US
├── Skill_Job_Analysis      # Skill demand likelihood for a given job title
└── Skill_Salary_Analysis   # Median salary by individual skill + demand frequency
```
 
Each sheet is a pivot table paired with an embedded chart for quick visual reference.
 
## 🔍 Overview
 
| Sheet | Description |
|---|---|
| **Salary_Vs_Skills** | Median salary vs. average number of skills per posting, by job title. e.g. Senior Data Scientist: ~$155K median, ~5.3 skills/job. |
| **Salary_Analysis** | Median salary by job title, split by US vs. Non-US postings, with an overall median. |
| **Skill_Job_Analysis** | Likelihood a given skill appears in postings for a specific role (e.g. Data Engineer: SQL 49%, Python 46%, AWS 30%). |
| **Skill_Salary_Analysis** | Median salary associated with individual skills (e.g. Python ~$98.5K, SQL ~$92.5K) alongside how often each skill is requested. |
 
## 📈 Key Findings
 
- **Seniority drives pay** — Senior-level roles (Senior Data Scientist, Senior Data Engineer) top the salary range at ~$147K–$155K median.
- **More skills ≠ more pay** — Data Engineers list the most skills per posting (~8.1) but aren't the top earners, so skill breadth doesn't scale linearly with salary.
- **Regional pay gaps** show up across nearly every role when comparing US vs. Non-US postings.
- **SQL and Python dominate** — both appear in roughly half of all relevant postings, regardless of specific role.
- **Niche tools can pay well** — Oracle and Tableau show competitive salaries despite lower demand frequency than general-purpose skills.
## 🛠️ Tech / Tools
 
- Microsoft Excel (pivot tables + charts)
- Source data: job posting listings aggregated by title and skill (source/date not currently documented in the workbook — see [Notes](#-notes))
## 📌 Notes
 
- "Grand Total" rows in each pivot represent blended/aggregate figures across all listed categories.
- Underlying dataset source and collection date should be added for reproducibility.
## 🚧 Possible Next Steps
 
- [ ] Document source and date range of underlying job posting data
- [ ] Add a combined role + skill + region cross-tab for deeper segmentation
- [ ] Standardize "skill likelihood" formatting (currently mixed decimal/percentage)
- [ ] Convert pivots to a script-based pipeline (e.g. pandas) for repeatable updates


# 3. Mobile Sales Dashboard

An interactive **Power BI** dashboard for analyzing mobile phone sales performance — covering revenue, quantity sold, transactions, customer ratings, and payment trends across brands, models, and cities.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)

## 📊 Overview

This report provides a single-page, at-a-glance view of mobile sales data, built to help stakeholders quickly spot trends in revenue, top-selling models, customer satisfaction, and regional performance.

## ✨ Features

- **KPI Cards** — Total Sales, Total Quantity, Transactions, and Average (at-a-glance summary metrics)
- **Sales by City** — Map visual showing geographic distribution of Total Sales
- **Sales Trend** — Line chart of Total Quantity over Month and Day
- **Top Models** — Clustered bar chart of Total Sales by Mobile Model
- **Payment Method Split** — Pie chart of Transactions by Payment Method
- **Customer Ratings** — Funnel chart of customer rating distribution
- **Day-of-Week Trend** — Area chart of Total Sales by Day Name
- **Brand Summary Table** — Total Sales, Total Quantity, and Transactions by Brand
- **Interactive Slicers** — Filter by Mobile Model, Payment Method, Brand, Day Name, and Month

## 🗂️ Data Model

| Table | Description |
|---|---|
| `Sales_Data` | Core fact table containing transaction-level mobile sales records |

**Key fields:** Brand, Mobile Model, City, Payment Method, Customer Ratings, Day Name, Month, Day

**Key measures:** Total Sales, Total Quantity, Transactions, Average

## 🛠️ Tools Used

- Power BI Desktop

## 🚀 Getting Started

1. Clone or download this repository.
2. Open `Mobile_Sales_Dashboard.pbix` in [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
3. If prompted, refresh the data source to reload the underlying dataset.
4. Use the slicers on the report page to filter by brand, model, payment method, day, or month.

## 📁 Repository Structure

```
├── Mobile_Sales_Dashboard.pbix   # Power BI report file
└── README.md                     # Project documentation
```

## 📌 Notes

- This is a single-page report ("Page 1") combining KPI cards, charts, a map, and a summary table.
- Data connections may need to be refreshed or repointed depending on where the source data resides.

## 📄 License

Add a license of your choice (e.g., MIT) if you plan to share this publicly.
