# Project 1: Data Cleaning & Preparation

## Overview

This project was completed as part of my Data Analytics Internship at DecodeLabs.

The objective was to clean and prepare a raw e-commerce dataset and ensure that the data was reliable and ready for analysis.

## Dataset

- **Records:** 1,200
- **Columns:** 14
- **Domain:** E-commerce
- **Tool:** Microsoft Excel

### Dataset Columns

The dataset contains information about:

- Order ID
- Date
- Customer ID
- Product
- Quantity
- Unit Price
- Shipping Address
- Payment Method
- Order Status
- Tracking Number
- Items in Cart
- Coupon Code
- Referral Source
- Total Price

## Data Cleaning Process

The following data quality checks and cleaning activities were performed:

- Reviewed the dataset structure and column meanings.
- Standardized column headers for consistency and readability.
- Removed unnecessary leading and trailing spaces from text fields using the `TRIM` function.
- Reviewed and confirmed appropriate data formats for dates, numbers, and text fields.
- Checked the dataset for duplicate records; no duplicates were identified.
- Identified missing values and found that blanks occurred only in the Coupon Code column.
- Replaced 309 blank Coupon Code values with `NO COUPON` to clearly represent orders where no coupon was applied.
- Checked categorical values for consistency.
- Validated `Total Price` against `Quantity × Unit Price`.
- Performed final checks on numerical values and date formatting.

## Data Integrity

The cleaned dataset was reviewed after the cleaning process to ensure that the identified issues were addressed and that the data remained consistent and suitable for further analysis.

## Project Files

- `Dataset for Data Analytics.xlsx` — Contains the raw dataset, cleaned dataset, and change log documentation.

## Key Learning

This project reinforced the importance of data integrity and showed that effective data cleaning is not simply about removing blanks and duplicates. It involves understanding the data, identifying genuine quality issues, making justified changes, and validating the results before analysis.
