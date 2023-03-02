## Bank Customer Analysis

This file contains code for analyzing customer churn in a bank dataset. The dataset is stored in a CSV file named "BankChurners.csv" and includes information about customer demographics, banking habits, and whether or not they churned (left) the bank.

### Requirements

The following Python libraries are required to run the code :

- pandas

- numpy

- scikit-learn

- matplotlib

- seaborn

- plotly

- dash

- dash-bootstrap-components

### Installation

To install the required libraries, run the following command:
pip install -r requirements.txt

### Data Cleaning

The data cleaning process is handled by the "Data Cleaning.ipnyb" script. This script reads in the "BankChurners.csv" file, removes any duplicates and the last two columns using the drop_duplicates() and drop() methods respectively. It also drops any rows that contain missing values. The script then applies label encoding and standardization using LabelEncoder and StandardScaler from scikit-learn, and normalization using MinMaxScaler.

### Dashboard

The dashboard displays various metrics related to customer churn in the bank dataset. The metrics are displayed using different charts and visualizations which shows the total number of customers, active and inactive customers, Gender, Average credit limit based on the income, Education status over attrition flag, people who were inactive for 12 month and how many times the bank contacted them, attrition flag measure based on the average of the credit limit, contact count in 12 month, Months on book and attrition count, inactivity and revolving balance. This dashboard allow you to interact with the data : https://public.tableau.com/views/DASHBOARD_16775931044680/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link
