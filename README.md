# DataScience-Cleaning-Transformation-Visualization
Data Science  Tasks Covering Data Cleaning ,Transformation ,And Visualization".
import pandas as pd

# Load the Iris dataset
df = pd.read_csv('Iris.csv')

# 1. Inspect the dataset
print("First five rows of the dataset:")
print(df.head())
print("\nSummary of missing values:")
print(df.isnull().sum())

# 2. Handle missing values (if any)
# For demonstration, we'll fill missing values with the median, although Iris dataset is usually clean
df.fillna(df.median(), inplace=True)

# 3. Remove duplicates (if any)
df = df.drop_duplicates()

# Display cleaned data
print("\nData after cleaning:")
print(df.info())
