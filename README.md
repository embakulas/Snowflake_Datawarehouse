# Snowflake_Datawarehouse

Banking Data Warehouse Project Requirements Document

1.	Project Overview:
    The goal of this project is to design and implement a data warehouse for a banking system. The data warehouse will facilitate efficient data storage, retrieval, and analysis for various business intelligence and reporting purposes. Data sources for the warehouse are CSV, JSON, and API’s. Amazon S3 buckets serve as a staging area for the data warehouse.
2.	Project Scope:
    The data warehouse will cover the following key aspects:
    1.	Data Sources:
    Capture transactional data from banking operations, including customer interactions, account activities, and financial transactions. Data comes in the format of CSV, JSON and API’s.
    2.	Data Categories:
    a.	Customer Data
    b.	Transactional Data
    c.	Account Data
    d.	Financial Data
    e.	Operational Data
    f.	Customer Feedback and Surveys
    g.	Digital Interactions
    3.	Data Warehouse Schema:
    Utilize a star schema with a central Transaction Fact Table and related Dimension Tables.
    4.	Dimensions Tables:
    a.	Account Dimension
    b.	Customer Dimension
    c.	Branch Dimension
    d.	Transaction Type Dimension
    e.	Risk and Compliance Dimension
    f.	Digital Interactions Dimension
    g.	Customer Feedback Dimension
    5.	Fact Table:
    Transaction Fact Table
3.	Detailed Requirements:
    1.	Transaction Fact Table:
    Capture transactional data. 
    Columns: Transaction_ID, Date, Account_ID, Customer_ID, Branch_ID, Transaction_Type, Risk_id, customer_feedback, Digital_interaction, amount
    2.	Account Dimension:
    Store account-related details, including account number, type (savings, checking), balance, open date, and close date.
    Columns: Account_id, Account_number, Account_Type, Open_date, close_date, Balance
    3.	Customer Dimension:
    Record customer information, including name, address, phone number, and email.
    Columns: customer_id, customer_name, address, phone_number, email, SSN,gender
    4.	Branch Dimension: 
    Store branch related details.
    Columns: Branch_id, branch_name, Location, Manager, assets
    5.	Transaction Type Dimension:
    Define various transaction types, such as deposit, withdrawal, and transfer.
    Columns: Transaction_Type_ID, Transaction Type
    6.	Risk and Compliance Dimension:
    Capture data related to Anti-Money Laundering (AML), Know Your Customer (KYC), and fraud detection.
    Columns: Risk_ID, customer_id, aml_status, KYC_status, fraud_status
    7.	Customer Feedback Dimension:
    Collect customer feedback data, including feedback type, ratings, and comments.
    Columns: feedback_id, customer_id, feedback_type, rating, comments..
