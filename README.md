# Hands-on Lab: Extract, Transform and Load GDP Data

## Introduction
In this practice project, you will utilize the skills acquired through the course to create a complete ETL pipeline for accessing data from a website and processing it to meet the requirements.

### Project Scenario
An international firm seeking to expand its business in various countries has recruited you as a junior Data Engineer. You are tasked with creating an automated script to extract the list of all countries ordered by their GDPs in billion USD (rounded to 2 decimal places), as reported by the International Monetary Fund (IMF). Since the IMF releases this evaluation biannually, this code will be used by the organization to extract updated information.

The required data is available at the following URL:
**URL:** `https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29`

The data must be accessible as a **CSV file** named **`Countries_by_GDP.csv`** and as a table in a database file named **`World_Economies.db`** with attributes **Country** and **`GDP_USD_billion`**.

Your boss wants you to demonstrate the success of this code by running a query on the database table to display only entries with economies exceeding 100 billion USD. Additionally, log the entire execution process in a file named **`etl_project_log.txt`**.

You must create a Python code file named **`etl_project_gdp.py`** that performs all required tasks.

## Objectives
You need to complete the following tasks for this project:

1. Write a data extraction function to retrieve relevant information from the specified URL.
2. Transform the available GDP information from 'Million USD' to 'Billion USD'.
3. Load the transformed information into the specified CSV file and database.
4. Execute the required query on the database.
5. Log the progress of the code with appropriate timestamps.

## Initial Setup
Before starting the code development, install the required libraries:

- **`requests`**: Used for accessing information from the URL.
- **`bs4`**: Contains the **`BeautifulSoup`** function used for web scraping.
- **`pandas`**: For processing extracted data and storing it in required formats, including databases.
- **`sqlite3`**: Required to create a database connection.
- **`numpy`**: Used for mathematical rounding operations as needed.
- **`datetime`**: Used for extracting timestamps for logging purposes.

## Importing Required Libraries
```python
import requests as req
import pandas as pd
import numpy as np
import datetime
import sqlite3
from bs4 import BeautifulSoup
```
## Known Entities
URL: https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29
Table Attributes: Initially ["Country", "GDP_USD_millions"] (will be modified in the transform function).
Database Name: World_Economies.db
Table Name: Countries_by_GDP
CSV Path: Countries_by_GDP.csv

## Conclusion
This project successfully demonstrates the creation of an ETL pipeline that extracts, transforms, and loads GDP data, making it accessible for further analysis and reporting.

## Credits

Code and Analysis: David Acosta Diaz
