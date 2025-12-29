# 📊 Data Science Job Market Analysis: Skills, Salaries & Trends

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="45"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="45"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="45"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sqlite/sqlite-original.svg" width="45"/>
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/84/Matplotlib_icon.svg" width="45"/>
  <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" width="45"/>
</p>


## 📌 Project Overview

This project performs an **end-to-end exploratory data analysis (EDA)** on a global **Data Science job market dataset** to uncover insights related to:

- 💰 Salary trends
- 🧠 Experience-level impact on compensation
- 🌍 Location-based hiring patterns
- 🏢 Company size and work setting influence
- 📈 Market evolution over time


## 🎯 Objectives

- Clean and standardize raw job market data using **Pandas**
- Perform detailed exploratory analysis using **Pandas**
- Visualize trends using **Matplotlib & Seaborn**
- Answer business-style analytical questions using **MySQL**
- Identify high-paying roles, in-demand experience levels, and geographic trends


## 🧰 Tech Stack

| Category | Tools |
|--------|-------|
| Data Cleaning | Pandas |
| Data Analysis | Pandas, SQL |
| Database | MySQL |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |


## 📂 Dataset Description

The dataset contains **global job postings** related to Data Science and AI roles with features such as:

- `work_year`
- `job_role`
- `job_category`
- `experience_level`
- `employment_type`
- `work_setting`
- `company_location`
- `company_size`
- `salary_in_usd`

> 💡 Only **USD-normalized salaries** were retained to ensure consistent salary analysis.


## 🧹 Data Cleaning (Pandas)

Data cleaning was performed entirely using **Pandas**, following real-world data quality practices:

### ✔ Cleaning Steps
- Removed redundant salary columns (`salary`, `salary_currency`)
- Dropped invalid salary values (negative or zero)
- Handled missing values in categorical features
- Removed duplicate job postings
- Standardized categorical values (experience level, employment type)
- Converted messy job titles into structured **job roles**
- Ensured consistent country naming
- Reordered columns for analytical clarity

### ✔ Result
A **clean, analysis-ready dataset** with consistent structure and realistic values.


## 📊 Exploratory Data Analysis & Visualization (Pandas)

Comprehensive EDA was conducted using **Pandas**, supported by **Matplotlib and Seaborn** for visualization.

### 🔍 Key Analysis Areas
- Overall salary distribution and skewness
- Experience level vs salary comparison
- Job role-based salary analysis
- Remote vs hybrid vs in-person work trends
- Company size impact on compensation
- Geographic job demand and salary variations
- Market segmentation using pivot tables and heatmaps
- Year-over-year salary and demand trends

Visualisations were also used for better understanding and analysis.

These visualizations helped translate raw numbers into **clear, interpretable insights**.


## 🗄️ SQL Analysis (MySQL)

The cleaned dataset was loaded into **MySQL** to answer **business-oriented analytical questions** using SQL.

### 📌 SQL Insights Covered
- Average & median salary by experience level
- Salary comparison across job roles
- Country-wise job distribution
- Highest paying roles per country
- Remote vs in-person salary comparison
- Role + experience level salary aggregation
- Identification of high-paying, high-demand roles

This step demonstrates the ability to:
> Translate analytical questions into efficient SQL queries.



## 🚀 Future Enhancements

- Interactive Streamlit dashboard
- Skill extraction using NLP
- Regional salary normalization
- Predictive salary modeling


## ⚙️ How to Run This Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/mrunmayee3108/Data-Science-Job-Market-Analysis.git
cd Data-Science-Job-Market-Analysis
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```


### 3️⃣ Run Data Cleaning & EDA (Pandas)

Open Jupyter Notebook and run all cells:

```bash
jupyter notebook
```

The notebook includes:

* Data cleaning using Pandas
* Exploratory Data Analysis (EDA)
* Visualizations using Matplotlib & Seaborn


## 🗄️ Load Cleaned Data into MySQL (Recommended CLI Method)

> ⚠️ **Note:** MySQL Workbench may fail for large CSV files.
> The **MySQL Command Line Client** is faster and more reliable.


### Step 1 — Navigate to MySQL `bin` folder (Windows)

```bash
cd "C:\Program Files\MySQL\MySQL Server 8.0\bin"
```


### Step 2 — Enable Local File Import

```bash
mysql -u your_username -p -D your_database_name -e "SET GLOBAL local_infile = 1;"
```

Enter your MySQL password when prompted.


### Step 3 — Log in with `local-infile` enabled

```bash
mysql -u your_username -p your_database_name --local-infile=1
```

This opens the MySQL shell (`mysql>`).


### Step 4 — Load the Cleaned CSV File

📌 **Important:** Use **forward slashes** in file paths on Windows.

```sql
LOAD DATA LOCAL INFILE 'C:/path/to/cleaned_job_market_data.csv'
INTO TABLE job_market
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;
```

**Explanation:**

* `LOAD DATA LOCAL INFILE` → bulk import command
* `IGNORE 1 ROWS` → skips the header row
* `ENCLOSED BY '"'` → handles quoted values

🚀 This method is **10–20× faster** than MySQL Workbench.


### Step 5 — Verify Import

```sql
SELECT COUNT(*) FROM job_market;
```


## 👥 Contributing

Pull requests are welcome.


## 📄 License

MIT License.


## 🙏 Acknowledgments

*  Kaggle (Dataset)

## ⭐ Support
If you like this project, consider giving the repository a ⭐ star on GitHub!

Author: Mrunmayee Sachin Potdar
