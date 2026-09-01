# Data Cleaning

This project focuses on cleaning and preparing a messy dataset for analysis using Python and Pandas.

## Objective

The objective of this project is to identify data quality issues and systematically transform a raw dataset into a clean, analysis-ready dataset.

## Tools and Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook

## Dataset

The dataset contains transaction information with the following columns:

- Transaction ID
- Item
- Quantity
- Price Per Unit
- Total Spent
- Payment Method
- Location
- Transaction Date

## Data Cleaning Process

The following data cleaning steps were performed:

### 1. Data Quality Assessment

The dataset was inspected to identify:

- Missing values
- Duplicate rows
- Data type issues
- Value range anomalies

### 2. Missing Value Handling

Missing values were handled using appropriate strategies based on the data type and characteristics of each column.

After cleaning, all missing values were successfully handled.

### 3. Duplicate Check

The dataset was checked for duplicate rows.

- Duplicate rows before cleaning: 0
- Duplicate rows after cleaning: 0

### 4. Data Standardisation

Categorical values were checked and standardised to ensure consistent formatting.

The dataset includes the following standardised categories:

**Items:**
- Coffee
- Cake
- Cookie
- Salad
- Smoothie
- Juice
- Sandwich
- Tea

**Payment Methods:**
- Credit Card
- Cash
- Digital Wallet

**Locations:**
- Takeaway
- In-Store

### 5. Data Type Correction

Data types were corrected to ensure that each column has an appropriate format.

- Transaction ID → String
- Quantity → Float
- Price Per Unit → Float
- Total Spent → Float
- Transaction Date → Datetime

### 6. Outlier Detection

The IQR method was used to detect potential outliers in numeric columns.

Potential outliers were examined to determine whether they represented genuine transactions or data errors.

The maximum value of 25 in the `Total Spent` column was retained because it represents a valid transaction value.

### 7. Data Validation

The cleaned dataset was validated to ensure there were:

- No missing values
- No duplicate rows
- No negative values in numeric columns
- Correct data types

## Before vs After Cleaning

| Metric | Before Cleaning | After Cleaning |
|--------|---------------|---------------|
| Row Count | 10,000 | 9,540 |
| Total Missing Values | 6,826 | 0 |
| Duplicate Rows | 0 | 0 |
| Data Type Accuracy | Incorrect | Correct |

## Final Dataset

The cleaned dataset contains:

- **9,540 rows**
- **8 columns**
- **0 missing values**
- **0 duplicate rows**

The final dataset is clean, consistent, and ready for further analysis.

## Conclusion

This project demonstrates the importance of data cleaning before analysis. Missing values were handled, data types were corrected, categorical values were standardised, and potential outliers were examined. The final dataset is reliable and suitable for further data analysis and visualization.
