# Layoffs-Data-Cleaning-and-EDA-in-MySQL
Cleaned and analyzed real-world layoffs data using MySQL. Project includes data cleaning, EDA, CTEs, window functions, trend analysis, and business insights.


# Layoffs Data Cleaning & Exploratory Data Analysis in MySQL

## Overview

This project focuses on cleaning and analyzing a real-world layoffs dataset using MySQL. The objective is to transform raw data into a clean and reliable format and uncover meaningful insights through SQL queries.

The project demonstrates practical data analytics skills such as data cleaning, data transformation, exploratory data analysis (EDA), aggregations, Common Table Expressions (CTEs), window functions, and business insight generation.

---

## Project Objectives

- Clean and standardize raw layoffs data
- Remove duplicate records
- Handle missing and null values
- Convert and validate data types
- Perform exploratory data analysis (EDA)
- Identify trends across companies, industries, countries, and time periods
- Generate actionable business insights

---

## Tools & Technologies

- MySQL
- MySQL Workbench
- SQL

---

## Dataset Description

The dataset contains information about layoffs from companies worldwide, including:

- Company
- Location
- Industry
- Total Laid Off
- Percentage Laid Off
- Date
- Stage
- Country
- Funds Raised (Millions)

---

## Data Cleaning Process

### 1. Remove Duplicates

Used `ROW_NUMBER()` and Common Table Expressions (CTEs) to identify and remove duplicate records.

### 2. Standardize Data

Performed the following cleaning operations:

- Trimmed company names
- Standardized industry names
- Standardized country names
- Fixed inconsistent values
- Converted date formats

### 3. Handle Missing Values

- Identified NULL values
- Populated missing values where possible
- Removed irrelevant records

### 4. Data Validation

Validated the dataset to ensure consistency and accuracy before analysis.

---

## Exploratory Data Analysis (EDA)

The following business questions were explored:

### Company Analysis

- Which companies laid off the most employees?
- Which companies experienced 100% layoffs?

### Industry Analysis

- Which industries were affected the most?
- Which industries had the highest layoffs over time?

### Country Analysis

- Which countries experienced the highest layoffs?
- What are the geographic layoff trends?

### Time Series Analysis

- Layoffs by year
- Layoffs by month
- Rolling total layoffs

### Advanced SQL Analysis

- Company rankings using Window Functions
- Top companies by year
- Cumulative layoffs over time

---

## Sample SQL Queries

### Top 10 Companies by Total Layoffs

```sql
SELECT company,
       SUM(total_laid_off) AS total_layoffs
FROM layoffs_staging2
GROUP BY company
ORDER BY total_layoffs DESC
LIMIT 10;
```

### Yearly Layoff Trends

```sql
SELECT YEAR(`date`) AS year,
       SUM(total_laid_off) AS total_layoffs
FROM layoffs_staging2
GROUP BY YEAR(`date`)
ORDER BY year;
```

### Top Industries by Layoffs

```sql
SELECT industry,
       SUM(total_laid_off) AS total_layoffs
FROM layoffs_staging2
GROUP BY industry
ORDER BY total_layoffs DESC;
```

---

## Key Insights

- Major technology companies recorded significant layoffs.
- Layoffs increased during periods of economic uncertainty.
- The United States accounted for the highest number of reported layoffs.
- Several startups experienced complete workforce reductions.
- Technology-related industries were among the most affected sectors.

---

## Skills Demonstrated

### SQL Skills

- Data Cleaning
- Data Transformation
- Data Validation
- Joins
- Aggregate Functions
- Window Functions
- Common Table Expressions (CTEs)
- Ranking Functions
- Date Functions

### Data Analysis Skills

- Exploratory Data Analysis (EDA)
- Trend Analysis
- Business Insight Generation
- Data Quality Assessment

---

## Project Structure

```text
Layoffs-Data-Cleaning-and-EDA-in-MySQL/
│
├── Dataset/
│   └── layoffs.csv
│
├── SQL Scripts/
│   ├── data_cleaning.sql
│   └── exploratory_data_analysis.sql
│
├── Screenshots/
│   ├── data_cleaning_results.png
│   ├── top_companies.png
│   ├── industry_analysis.png
│   └── yearly_trends.png
│
└── README.md
```

---

## Screenshots

### Data Cleaning Output

_Add screenshot here_

### Top Companies by Layoffs

_Add screenshot here_

### Yearly Layoff Trends

_Add screenshot here_

### Industry Analysis

_Add screenshot here_

---

## Learning Outcomes

Through this project, I gained hands-on experience in:

- Cleaning messy real-world datasets
- Writing complex SQL queries
- Using Window Functions and CTEs
- Performing exploratory data analysis
- Extracting business insights from raw data
- Structuring SQL projects for professional portfolios

---

## Author
 
**Md Rashidul Islam**
 
- LinkedIn: [Rashidul Islam](https://www.linkedin.com/in/rashidul-islam-337228b1/)
- GitHub: [rashidul738](https://github.com/rashidul738)
 
Feel free to connect with me for discussions about SQL, Data Analytics, Data Cleaning, EDA, and Business Intelligence.
