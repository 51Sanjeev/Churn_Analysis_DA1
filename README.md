# Churn_Analysis_DA1
### (Customer Churn Analysis)

A data analysis project focused on understanding **customer churn** by combining customer demographics, subscription/billing information, and customer support interactions.

The project uses **Python, Pandas, SQLite, SQL, and data visualization** to clean, transform, analyze, and extract insights from customer data.

---

## 📌 Project Overview

Customer churn is an important business problem because retaining existing customers is generally more valuable than continuously acquiring new ones.

In this project, customer data from multiple sources is combined into a single analytical dataset to investigate factors associated with churn, including:

* Customer demographics
* Subscription and contract details
* Monthly charges
* Customer lifetime value (CLTV)
* Cancellation information
* Customer support interactions
* Escalations
* CSAT scores
* Complaint frequency

The final dataset is used to perform exploratory data analysis and identify patterns related to customer churn.

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas** – Data cleaning and manipulation
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **SQLite** – Database storage and querying
* **SQL** – Data extraction and transformation
* **Jupyter Notebook** – Analysis environment
* **Excel** – Source data preparation and inspection

---

## 📂 Project Structure

```text
Customer-Churn-Analysis/
│
├── Churn_Analysis.ipynb
│
├── customer_churn.db
├── customer_churn_data_raw.xlsx
│
├── db_customer_new.xlsx
├── db_subscription_new.xlsx
├── db_support_new.xlsx
│
├── exported_churn_data.csv
│
└── test_database.sqlite
```

---

## 📄 File Description

### `Churn_Analysis.ipynb`

Main Jupyter Notebook containing the complete churn analysis workflow.

The notebook covers data loading, cleaning, database operations, merging datasets, feature engineering, exploratory analysis, and visualization.

---

### `customer_churn.db`

The main SQLite database used for the project.

It contains three primary tables:

| Table             | Records |
| ----------------- | ------: |
| `db_customer`     |     121 |
| `db_subscription` |     121 |
| `db_support`      |      64 |

The database represents the consolidated/final version of the customer, subscription, and support data.

---

### `customer_churn_data_raw.xlsx`

Initial/raw Excel workbook containing three sheets:

* `db_customer`
* `db_subscription`
* `db_support`

This file represents the earlier version of the dataset before the data was expanded and cleaned.

---

### `db_customer_new.xlsx`

Customer master data containing demographic and personal information such as:

* `customerid`
* `name`
* `country`
* `state`
* `gender`
* `dob`
* `interests`
* `pincode`

Contains approximately **100 customer records**.

---

### `db_subscription_new.xlsx`

Subscription and billing information containing fields related to:

* Subscription dates
* Subscription type
* Plan
* Contract
* Cancellation information
* Monthly charges
* CLTV
* Churn score

Contains approximately **100 records**.

---

### `db_support_new.xlsx`

Customer support interaction data containing information such as:

* Complaint date
* Escalations
* CSAT score
* Customer comments

Contains approximately **55 support records**.

---

### `exported_churn_data.csv`

Final analytical dataset created after combining the customer, subscription, and support data.

It contains:

* **121 rows**
* **21 columns**

It also includes derived analytical features such as:

* `churn_flag`
* `complaint_count`

This dataset represents the final feature-engineered data used for analysis.

---

### `test_database.sqlite`

A small SQLite database created for testing database connectivity and SQLite operations.

It contains a separate `users` table and is **not part of the customer churn analysis**.

---

## 🔄 Data Analysis Workflow

```text
Raw Excel Data
      ↓
Data Cleaning
      ↓
Data Validation
      ↓
SQLite Database
      ↓
Customer + Subscription + Support
      ↓
Data Merging
      ↓
Feature Engineering
      ↓
Exploratory Data Analysis
      ↓
Churn Analysis & Visualization
      ↓
Final Analytical Dataset
```

---

## 🔍 Key Analysis Areas

The project investigates several potential factors related to customer churn.

### Customer Demographics

Analysis of churn across:

* Gender
* State
* Country
* Customer age
* Customer interests

### Subscription Analysis

Analysis of churn based on:

* Subscription type
* Plan
* Contract type
* Monthly charges
* Customer lifetime value
* Subscription duration

### Customer Support Analysis

Analysis of whether customer service interactions are associated with churn, including:

* Number of complaints
* Escalations
* CSAT scores
* Support interactions

### Churn Analysis

The project calculates and visualizes:

* Overall churn rate
* Churn by plan
* Churn by contract
* Churn by state
* Churn by subscription characteristics
* Churn by customer support activity
* Revenue associated with different customer segments

---

## 📊 Feature Engineering

Additional features are created from the original data to make the analysis more meaningful.

Examples include:

* `churn_flag` – identifies whether a customer has churned
* `complaint_count` – number of support complaints associated with a customer
* Customer age
* Cancellation month
* Other derived analytical fields

These features allow customer-level data to be grouped and compared more effectively.

---

## 🗄️ Database Structure

The SQLite database follows a relational structure where the common key is:

```text
customerid
```

The main relationships can be represented as:

```text
db_customer
     │
     │ customerid
     ↓
db_subscription
     │
     │ customerid
     ↓
db_support
```

The three datasets are ultimately combined using `customerid` to create the final analytical dataset.

---

## 🎯 Project Objective

The primary objective is to use customer data to answer questions such as:

* Which customers are more likely to churn?
* Which subscription plans have higher churn?
* Does contract type influence customer retention?
* Are higher monthly charges associated with churn?
* Does customer support activity relate to churn?
* Do escalations or poor CSAT scores indicate higher churn?
* Which customer segments generate the most revenue?
* What patterns can help a business improve customer retention?

---

## 📈 Outcome

The project demonstrates an end-to-end data analysis workflow:

**Data Collection → Data Cleaning → Database Management → Data Transformation → Feature Engineering → Exploratory Data Analysis → Visualization → Business Insights**

It showcases practical experience working with **Python, Pandas, SQL, SQLite, Excel, and data visualization** on a realistic business problem.

## ⭐ Project Focus
This project was built as a practical demonstration of applying data analysis techniques to a real-world business problem and converting raw customer data into meaningful insights for understanding and reducing customer churn.

This project was built as a practical demonstration of applying data analysis techniques to a real-world business problem and converting raw customer data into meaningful insights for understanding and reducing customer churn.
