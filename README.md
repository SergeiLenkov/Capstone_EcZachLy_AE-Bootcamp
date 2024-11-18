# Capstone_EcZachLy_AE-Bootcamp
This repo is my capstone project for Analytics Engineer Bootcamp provided by Zach Wilson (EcZachly Inc)

**Project Specification: Automated Stock Analysis System**

**Introduction**

This project aims to automate the identification of promising stocks based on dividend increase announcements over the last three days. The system integrates with multiple APIs, databases, and data visualization tools to extract, process, and present financial insights effectively.

**Objectives**

The primary objectives of the project are:

* Fetch stocks with dividend increase announcements from NewsAPI, including the percentage of increase (if available).  
* Store the extracted data in Trino \+ Snowflake (on Trino) for further processing.  
* Retrieve financial ratios for the identified stocks using FinancialModelingPrep (site.financialmodelingprep.com).  
* Use dbt (Data Build Tool) to model and transform data into dimensional and fact tables.  
* Visualize the top 10 prospective stocks in Tableau.

**Workflow**

**Step 1: Data Extraction**

Use NewsAPI to fetch news articles related to dividend increase announcements over the last 3 days. Ensure to extract relevant metadata, including stock ticker, company name, and the percentage of dividend increase (if available).

**Step 2: Data Storage**  
Load the extracted data into Trino \+ Snowflake (on Trino). This includes creating a staging table for raw data.

**Step 3: Financial Data Enrichment**  
For each stock identified in Step 1, use FinancialModelingPrep (site.financialmodelingprep.com) to fetch financial ratios such as P/E ratio, debt-to-equity ratio, and others. Store this data in the database.

**Step 4: Data Modeling**  
Use dbt to create dimensional and fact tables:

* Dimensional Table: Stock details (Ticker, company name, stock exchange, sector, etc.).  
* Fact Table: Ticker, Date, Financial metrics, Dividend increase percentage announcement, % of increase  
* (Future improvement \- out of scope of the bootcamp \- current portfolio of purchased stocks) \*\*\*

**Step 5: Data Visualization**  
5\. Connect the transformed data in Snowflake/Trino to Tableau and create visualizations to identify the top 10 stocks based on defined metrics.

**Tools and Technologies**

* **APIs**: NewsAPI for news data, FinancialModelingPrep (site.financialmodelingprep.com) for financial data.  
* **Database:** Snowflake/Trino for data storage.  
* **ETL Tool:** dbt for data transformation and modeling.  
* **Visualization:** Tableau for data visualization and insights.

**Deliverables**

* Scripts to extract and load data from NewsAPI and FinancialModelingPrep (site.financialmodelingprep.com).  
* Trino \+ Snowflake (on Trino) database with staged, dimensional, and fact tables.  
* dbt project for data transformation and modeling.  
* Tableau dashboard visualizing the top 10 prospective stocks.

**Timeline**

* **Day 1**: Set up APIs and database connections.  
* **Day 2:** Implement data extraction from NewsAPI and load the data to the database.  
* **Day 3:** Retrieve and store financial ratios from FinancialModelingPrep (site.financialmodelingprep.com). (additional pipeline)  
* **Day 4:** Develop dbt models and validate data integrity.  
* **Day 5:** Create Tableau dashboard and finalize the project.
