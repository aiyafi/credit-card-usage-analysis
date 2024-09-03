# Credit Card Customer Churn Analysis

## Brief Description

This project analyzes credit card customer data to predict and understand the reasons behind customer churn. It uses various exploratory data analysis techniques to gain insights from the bank's dataset.

## Dataset Description

The dataset used in this project is 'BankChurners.csv'. It contains information about credit card customers, including:

- Customer demographics (age, gender, education level, marital status)
- Account information (credit limit, total transaction amount, months on book)
- Churn status (existing customer or attrited customer)

Key features of the dataset:
- 10,127 entries
- Mix of numerical and categorical variables
- 16% of customers in the dataset have churned

## Installation

To run this project, you need Python and the following Python packages:

## Usage

1. Import the required libraries:
   ```python
   import pandas as pd
   import numpy as np
   import matplotlib.pyplot as plt
   import seaborn as sns
   from sklearn.model_selection import train_test_split
   from sklearn.preprocessing import StandardScaler
   ```

2. Load the dataset:
   ```python
   data = pd.read_csv('BankChurners.csv')
   ```

3. Explore the data using various functions and visualizations:
   - Use `data.info()` and `data.describe()` for a quick overview
   - Use `data.head()` and `data.tail()` to view sample rows
   - Create visualizations using matplotlib and seaborn for deeper insights

4. The notebook includes various exploratory analyses:
   - Histograms for continuous variables
   - Scatter plots to explore relationships between variables
   - Pie charts and bar graphs for categorical variables
   - Correlation analysis using heatmaps
   - Boxplots for distribution and outlier detection

5. Preprocess the data and split it into training and testing sets:
   ```python
   X = data.drop('Attrition_Flag', axis=1)
   y = data['Attrition_Flag']
   X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
   ```

6. Train and evaluate machine learning models to predict customer churn.

7. Interpret the results to understand factors contributing to customer churn and identify potential areas for improvement in customer retention strategies.

Note: Make sure to adjust file paths as necessary when running the code on your local machine.