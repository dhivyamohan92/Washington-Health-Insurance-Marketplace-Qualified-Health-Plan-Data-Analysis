# Washington-Health-Insurance-Marketplace-Qualified-Health-Plan-Data-Analysis

# Washington State Qualified Health Plan (QHP) Data Analysis Using Python

## Project Overview

This project analyzes Washington State Qualified Health Plan (QHP) data to understand health insurance plan distribution, age-based rate variations, benefit coverage, issuer-level pricing differences, and data quality.

Using Python, Pandas, NumPy, Matplotlib, and Seaborn, the project applies data cleaning, exploratory data analysis (EDA), data validation, and visualization techniques to identify patterns and generate actionable business insights.

## Business Objectives

- Analyze health insurance plan distribution by plan type and metal level.
- Examine rate variations across age groups and geographic rating areas.
- Compare average rates across insurance issuers.
- Evaluate benefit coverage and Essential Health Benefit (EHB) classifications.
- Investigate missing values, zero-rate records, and potential data-quality issues.
- Identify the limitations affecting affordability comparisons and plan selection.

## Tools and Technologies

- **Python** – Data analysis and processing
- **Pandas** – Data cleaning, transformation, grouping, and aggregation
- **NumPy** – Numerical analysis
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization and dashboard charts
- **Plotly** – Interactive dashboard visualization
- **Google Colab** – Cloud-based development environment
- **Excel** – Source data format

## Dataset Description

The project uses a Washington State QHP Excel workbook containing five worksheets:

| Worksheet | Description |
|---|---|
| Plans | Plan characteristics, issuer information, metal levels, and plan types |
| Rates | Individual rates by age, plan, issuer, and rating area |
| Benefits | Benefit coverage, EHB classifications, and quantity limits |
| Networks | Issuer network information and network classifications |
| ServiceAreas | Issuer service areas and county-level information |

The dataset includes 328 plan records, 28,713 rate records, 23,116 benefit records, 20 network records, and 477 service-area records.

## Project Methodology

### 1. Data Loading and Understanding
- Loaded the Excel workbook into Pandas DataFrames.
- Inspected worksheet dimensions, column names, and data types.
- Reviewed the structure and meaning of the available fields.

### 2. Data Cleaning
- Identified duplicate records and completely empty columns.
- Standardized selected text fields.
- Converted actuarial values and relevant numeric fields for analysis.
- Examined missing values without automatically replacing potentially meaningful missing data.

### 3. Exploratory Data Analysis
- Analyzed plan distribution by type and metal level.
- Examined age-based rate patterns.
- Compared average rates by issuer and rating area.
- Evaluated benefit coverage and EHB classifications.
- Reviewed network and service-area distributions.

### 4. Data Validation
- Validated issuer IDs across the five worksheets.
- Matched plan IDs between Plans, Rates, and Benefits by removing numeric suffixes where appropriate.
- Investigated zero-rate records and missing data.
- Confirmed that network IDs can be reused across issuers.

### 5. Data Visualization
Created dashboard charts to communicate the main findings:

1. Plan Distribution by Type
2. Plan Distribution by Metal Level
3. Average Rate by Age
4. Benefit Coverage Status
5. Top 10 Issuers by Average Rate

Interactive Plotly visualizations were also developed to support hovering, zooming, and exploring chart values.

## Key Business Insights

- **Plan Distribution:** EPO plans account for 71.95% of plan records, followed by HMO at 25.91% and PPO at 2.13%.
- **Metal-Level Distribution:** Silver plans account for 38.41% of records, followed by Gold at 34.76% and Expanded Bronze at 22.87%.
- **Age-Based Rates:** The average rate increases from approximately 347.45 for ages 0–14 to 1,345.60 for ages 64 and over, a difference of approximately 3.87 times.
- **Geographic Variation:** Rating Area 2 has the highest average rate at approximately 728.22, while Rating Area 7 has the lowest at approximately 626.20.
- **Issuer Comparison:** Average rates vary across issuers. Comparisons within similar age groups and plan categories are needed to assess price competitiveness.
- **Benefit Coverage:** Approximately 81.1% of benefit records are marked as covered.
- **Potential Dental Coverage Gap:** Basic Dental Care – Adult is marked not covered in 321 of 328 records.
- **Tobacco Analysis:** All rate records are classified as “No Preference,” preventing a comparison of tobacco-related rate differences.
- **Data Quality:** Missing deductible and maximum out-of-pocket values limit reliable comparisons of total consumer costs.
- **Zero-Rate Investigation:** Zero
