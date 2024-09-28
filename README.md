GDP Data ETL Project
Project Overview
In this project, a complete ETL (Extract, Transform, Load) pipeline was created to extract GDP data for different countries from a given website, transform it as required, and load it into both a CSV file and a SQLite database.

The goal is to automate the process of retrieving and processing GDP data, making it accessible for further analysis. The data is fetched from a web archive of a Wikipedia page that lists countries' GDPs, transforms it to meet specific requirements, and saves the results to a database and CSV file.

Project Scenario
An international firm looking to expand its business globally has recruited you as a Junior Data Engineer. You are tasked with creating an automated script to extract the list of all countries in order of their GDPs in billion USDs (rounded to 2 decimal places), as provided by the International Monetary Fund (IMF). The code will be used to extract this information as it is updated bi-annually.

The GDP data is available at the following URL:

URL: List of countries by GDP (nominal)

The final data must be accessible in two formats:

CSV file named Countries_by_GDP.csv.
SQLite database named World_Economies.db with a table named Countries_by_GDP containing the columns Country and GDP_USD_billion.
Project Requirements
Create a Python script named etl_project_gdp.py.
The script should extract, transform, and load the data into the required formats.
Demonstrate the success of the code by running a query to display countries with a GDP greater than 100 billion USD.
Log all the steps of the execution in a file named etl_project_log.txt.
