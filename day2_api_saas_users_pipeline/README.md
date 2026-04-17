# 📊 Day 2 — SaaS Users Data Pipeline

## 🚀 Overview
This project is part of my **30 Days of Data Analytics Challenge**.

On Day 2, I built a Python-based ETL pipeline to fetch user data from a live API, transform nested JSON into a structured format, and load it into a Pandas DataFrame for analysis.

## 🎯 Objective
- Extract user data from an API  
- Transform nested JSON into a flat structure  
- Load the data into a Pandas DataFrame  

## 🏗️ Pipeline Architecture
API → Extract → Transform → Load

- Extract → Fetch data using requests  
- Transform → Clean and flatten JSON response  
- Load → Store data in Pandas DataFrame / CSV  

## 🧰 Tech Stack
- Python  
- requests  
- pandas  

## 📁 Project Structure
day2_saas_users/
│
├── saas_users_pipeline.py   # Main ETL pipeline script
├── saas_users.csv           # Output dataset
└── README.md                # Project documentation

## ⚙️ How to Run
1. Install dependencies  
pip install pandas requests  

2. Run the script  
python saas_users_pipeline.py  

## 📊 Sample Output
| full_name  | email           | country | age |
|-----------|----------------|--------|-----|
| John Doe  | john@email.com | USA    | 28  |
| Jane Smith| jane@email.com | UK     | 32  |

## 🔄 Data Transformation
Raw API JSON (nested):
{
  "name": {"first": "John", "last": "Doe"},
  "location": {"country": "USA"}
}

Transformed into:
- full_name  
- email  
- country  
- age  
- signup_date  

## 🧠 Key Learnings
- Extracting data from APIs using requests  
- Handling HTTP errors with raise_for_status()  
- JSON flattening for structured analysis  
- Building a basic ETL pipeline  
- Converting raw data into analysis-ready format  

## ⚠️ Error Handling
- Implemented try-except block  
- Used response.raise_for_status() to catch API errors  
- Ensures pipeline reliability  

## 🚀 Future Improvements
- Add logging instead of print statements  
- Store data in a database (PostgreSQL)  
- Automate pipeline using scheduler (cron / Airflow)  
- Perform user segmentation and analysis  

## 📌 Conclusion
This project demonstrates how raw API data can be transformed into meaningful datasets, forming the foundation for real-world SaaS analytics workflows.
