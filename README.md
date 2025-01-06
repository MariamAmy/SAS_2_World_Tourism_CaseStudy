# World Tourism Data Preparation and Analysis

## Overview
This project focuses on preparing and analyzing tourism data by cleaning, transforming, and merging datasets. The process involves handling missing data, standardizing columns, and performing calculations for tourism metrics. The final dataset is validated with frequency distributions and descriptive statistics.

## Project Steps

### 1. **Data Preparation**
- The dataset `work.tourism` is cleaned and transformed into `cleaned_tourism`.
- **Key Cleaning Steps:**
  - Retain country names where missing.
  - Identify tourism types (`Inbound` and `Outbound`).
  - Remove rows where country names match tourism types.
  - Standardize the `Series` column to uppercase.
  - Handle missing values by replacing placeholders.
  - Convert financial units (`Millions` and `Thousands`) into numerical values.
  - Create a formatted `Category` for easier analysis.

- **Final Transformations:**
  - Values for 2014 are converted into numeric data (`Y2014`).
  - The column `Y2014` is formatted with commas for readability.

---

### 2. **Defining Formats**
- A custom format is created using `PROC FORMAT` to classify continents:
  - North America, South America, Europe, Africa, Asia, Oceania, and Antarctica.

---

### 3. **Data Integration**
- The cleaned tourism data is merged with a country information dataset (`work.country_info`).
- Sorting is performed before merging to ensure data integrity.
- **Outputs:**
  - `final_tourism`: Contains merged data where both datasets matched.
  - `nocountryfound`: Lists countries present in the tourism dataset but not in the country information dataset.

---

### 4. **Data Validation**
- **Unmatched Countries:** A list of countries not found in the `country_info` table is printed.
- **Frequency Counts:** The frequency of key variables (`Category`, `Series`, `Tourism_Type`, `Continent`) is calculated using `PROC FREQ`.
- **Descriptive Statistics:** The mean, minimum, and maximum values for `Y2014` are calculated using `PROC MEANS`.

---

## Required Software
- **SAS (Base SAS)**

---

## Files Included
- **Input:** `work.tourism`, `work.country_info`
- **Output:** `cleaned_tourism`, `final_tourism`, `nocountryfound`
- **SAS Script:** Contains all code for data cleaning, transformation, and analysis.

---

## How to Use
1. Load the `work.tourism` and `work.country_info` datasets into your SAS environment.
2. Run the SAS script provided to clean and prepare the data.
3. Review the generated datasets (`final_tourism` and `nocountryfound`).
4. Check the output from frequency and statistical tests for validation.
5. Modify data sources as needed for different analysis scopes.

---

## Conclusion
This project prepares tourism data for analysis by cleaning and standardizing the dataset, merging it with country information, and validating the results. It provides a foundation for further exploration of tourism trends and patterns.
