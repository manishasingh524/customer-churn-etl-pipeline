# Customer Churn ETL Pipeline

## Project Overview
This project demonstrates an end-to-end ETL (Extract, Transform, Load) pipeline built using Python (Pandas) on a Customer Churn dataset.

The objective of this project is to clean, validate, and normalize raw customer data into structured relational tables while ensuring data integrity and consistency.

## Tech Stack
- Python
- Pandas
- Google Colab / Jupyter Notebook
- CSV Dataset

## ETL Process

### 1. Extract
- Loaded raw dataset using pandas.read_csv()
- Explored dataset using:
  - df.head()
  - df.info()
  - df.shape
- Stored original row count for validation

### 2. Transform

#### Data Cleaning
- Checked for missing values
- Removed duplicate rows
- Standardized column names
- Verified data types

#### Feature Engineering
Created derived columns:
- high_value_customer (based on total_spend)
- long_tenure (based on tenure)

#### Data Validation
- Original Rows: 64,374
- Cleaned Rows: 64,374
- Rows Removed: 0

No missing values or duplicate records were found in the dataset.



### 3. Load (Data Normalization)

The cleaned dataset was split into three structured relational tables:

#### Customers Table
- customer_id
- age
- gender
- subscription_type
- contract_length

Rows: 64,374

#### Usage Table
- customer_id
- tenure
- usage_frequency
- support_calls
- payment_delay
- last_interaction

Rows: 64,374

#### Churn Table
- customer_id
- total_spend
- churn
- high_value_customer
- long_tenure

Rows: 64,374



## Data Integrity Validation
- All tables contain consistent row counts
- No data loss during transformation
- Referential integrity maintained using customer_id
- Row validation check passed successfully



## Key Skills Demonstrated
- ETL Pipeline Development
- Data Cleaning and Validation
- Feature Engineering
- Data Normalization
- Data Integrity Verification
- Relational Data Structuring



## Conclusion
This project demonstrates the ability to design and implement a structured ETL pipeline using Python, applying data engineering best practices to produce clean, validated, and analysis-ready data.
