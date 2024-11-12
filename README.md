# DS-2002-Project
DS midterm project, fall 2024.
Connor Powell
Spy8dg


This repository contains an etl_pipeline that builds a data warehouse from retail sale data. It extracts, transforms, and loads data into MongoDB and SQLite databases for analysis.
The etl_pipeline works to extract data from the retail_sales_dataset.csv and then transforms it to create dimension tables for customer, product, date, and fact table for sales.
  - to run: /usr/local/bin/python3 setup.py


required libraries: pandas, pymongo, sqlite3, certifi.
