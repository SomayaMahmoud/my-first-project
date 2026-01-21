# my-first-project

Project Overview
This project demonstrates a comprehensive data cleaning pipeline using Python and Pandas. The goal is to transform a "dirty" dataset containing cafe transaction records into a clean, analysis-ready format. The notebook addresses common data quality issues including missing values, incorrect formatting, and logical inconsistencies in financial records.

Dataset Description
The dataset used is dirty_cafe_sales.csv, which consists of 10,000 transaction records with the following columns:
Transaction ID: Unique identifier for each sale.
Item: The product sold (e.g., Coffee, Cake, Juice).
Quantity: Number of items purchased.
Price Per Unit: Unit price of the item.
Total Spent: Total transaction value (often requires recalculation).
Payment Method: Method used (e.g., Credit Card, Cash, Digital Wallet).
Location: Order type (e.g., Takeaway, In-store).
Transaction Date: The date the sale occurred.

Cleaning Steps Implemented
The notebook performs the following operations to ensure data integrity:
Initial Assessment: Loading data and inspecting null counts, data types, and statistical summaries.
Type Conversion: Converting Quantity and Price Per Unit into numeric formats to allow for calculations.
Handling Placeholders: Identifying and replacing string-based errors like "ERROR" and "UNKNOWN" with null values (NaN).

Imputation:
Categorical Data: Filling missing Item, Payment Method, and Location values using the mode (most frequent value).
Numerical Data: Filling missing Quantity and Price Per Unit using the median.
Dates: Filling missing Transaction Date using the mode.
Logical Validation: Recalculating Total Spent by multiplying Quantity by Price Per Unit to ensure accuracy across all records.
Outlier Detection: Using the Interquartile Range (IQR) method to identify anomalies in spending and quantities.


Requirements
To run this notebook, you will need the following Python libraries:
pandas
numpy
matplotlib
seaborn
