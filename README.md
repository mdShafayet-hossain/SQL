🧹 SQL Data Cleaning Project – World Layoffs Dataset
📌 Project Overview

This project demonstrates how to clean and preprocess raw data using SQL. The dataset contains information about global layoffs, including company names, industries, locations, number of employees laid off, and funding details.

The main goal of this project was to transform messy, inconsistent, and incomplete data into a clean and analysis-ready format.

⚙️ Steps Performed
1. Setup

Created a staging table (layoffs_staging) to preserve raw data.

Worked on a copy of the dataset to avoid altering the original.

2. Remove Duplicates

Identified duplicates using ROW_NUMBER() with PARTITION BY.

Deleted duplicate records to keep only unique entries.

3. Standardize Data

Fixed inconsistent text entries in industries (e.g., "Crypto Currency" → "Crypto").

Cleaned up country names (e.g., removed trailing periods like United States.).

Converted date column from TEXT to DATE format.

Replaced blank values in industry with NULL for better handling.

4. Handle Missing Values

Filled missing industry values using company-level matches.

Kept NULL values in total_laid_off, percentage_laid_off, and funds_raised_millions for accurate analysis.

5. Remove Irrelevant Data

Deleted rows where both total_laid_off and percentage_laid_off were NULL (useless data).

Dropped the temporary row_num column used for duplicate detection.

📊 Final Output

The final cleaned dataset (layoffs_staging2) is:

Free of duplicates

Standardized for industries, countries, and dates

Ready for Exploratory Data Analysis (EDA) and reporting

📂 Project Files

Project.Data Cleaning.sql → SQL script containing the full cleaning process.

🚀 How to Use

Import the dataset into MySQL (or any SQL-compatible DBMS).

Run the queries in Project.Data Cleaning.sql step by step.

Use the final table layoffs_staging2 for analysis.

🔑 Key Learnings

Practical application of SQL window functions (ROW_NUMBER).

Handling duplicates and missing data.

Data standardization techniques in SQL.

Preparing raw data for real-world analytics.
