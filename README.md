# DS-2002-Project
DS midterm project, fall 2024.
Connor Powell
Spy8dg


This repository contains an etl_pipeline that builds a data warehouse from retail sale data. It extracts, transforms, and loads data into MongoDB and SQLite databases for analysis.
  - to run: /usr/local/bin/python3 setup.py
  - required libraries: pandas, pymongo, sqlite3, certifi.

Data Transformation:
Converts the Date column to datetime format and adds Month and Season columns
    Splits-
        dim_customer: Unique customer records.
        dim_product: Unique product categories.
        dim_date: Unique date records, categorized by Month and Season.
        Creates a fact_sales table with foreign keys (CustomerID, ProductID, DateID) and metrics like Quantity, PricePerUnit, and Total Amount.
        
Loading:
  MongoDB: Loads the raw data into a collection (RetailSales). Sample aggregation queries for total sales by category and monthly sales totals are provided.
  SQLite: Loads DimCustomer, DimProduct, DimDate, and FactSales tables into data_mart.db

Output: Total sales by product category
        Monthly sales totals
        Row counts for dimension tables
