📊 Customer Churn ETL 

📌 Project Overview
This project demonstrates an end-to-end ETL (Extract, Transform, Load) pipeline built using Python (Pandas) on a Customer Churn dataset.
The objective is to clean, validate, and normalize raw customer data into structured relational tables while ensuring data integrity and consistency.

🛠️ Tech Stack
Python
Pandas
Google Colab / Jupyter Notebook
CSV Data Source

🔄 ETL Process
1️⃣ Extract
Loaded raw dataset from CSV file using pandas.read_csv()
Inspected dataset structure using:
df.head()
df.info()
df.shape

2️⃣ Transform
✅ Data Cleaning
Removed missing values using:
df.dropna()
Removed duplicate records using:
df.drop_duplicates()
✅ Data Type Validation
Verified column data types
Ensured numerical columns are properly formatted
Confirmed no unexpected null values
✅ Data Validation
Stored original row count before cleaning
Compared row counts after transformation
Verified:
No data loss
No unintended row removal
No duplication
Validation Results:
Original Rows: 64,374
Cleaned Rows: 64,374
Rows Removed: 0
Dataset contained no missing or duplicate values.

3️⃣ Load (Data Normalization)
The cleaned dataset was normalized into three relational tables:
📁 Customers Table
Contains:
customer_id
demographic information
account details
Shape: (64,374, 5)
📁 Usage Table
Contains:
customer_id
service usage metrics
billing information
Shape: (64,374, 6)
📁 Churn Table
Contains:
customer_id
churn status
churn-related attributes
Shape: (64,374, 5)
✅ Data Integrity Validation
After splitting tables:
All tables contain 64,374 rows
Row counts are consistent across all tables
No data loss occurred during normalization
Referential integrity maintained via customer_id
Validation successful.

📊 Final Dataset Structure
Table      customers    Usage     churn
Rows        64,374     64,374     64,374
Columns       5           6        5

🚀 Future Improvements
     1.Export tables to SQL database
     2.Add ER diagram
     3.Implement automated validation checks
     4.Build churn prediction model
     5.Deploy pipeline as reusable script

📌 Conclusion
This project demonstrates a structured and validated ETL pipeline ensuring high-quality, normalized, and analysis-ready data suitable for downstream analytics or machine learning applications.📊 Customer Churn ETL Pipeline


This project demonstrates a structured and validated ETL pipeline ensuring high-quality, normalized, and analysis-ready data suitable for downstream analytics or machine learning applications.
