# Data-manupulation-with-python
#pandas library to manipulate data
# TASK-2 GIVEN BY Main Flow Services and Technologies
# 1.Load the CSV file into a Pandas DataFrame.
# 2.Filter data based on specific conditions.
# 3.Handle missing values.
# 4.Calculate summary statistics.


# 1. Load the CSV file into a Pandas DataFrame (heartdisease data set)
import pandas as pd
# Load the CSV file into a DataFrame
df = pd.read_csv('/content/heart - heart.csv')  #df means dataframe
# Display the first few rows of the DataFrame
print(df.head())

# 2. Filter data based on specific conditions
# Filter rows where column 'age' is greater than 30
filtered_df = df[df['age'] > 30]
# Display the filtered DataFrame
print(filtered_df)

# 3. Handle missing values
# There are various ways to handle missing values, such as
# filling them with a specific value or
# dropping the rows/columns with missing values.
# 1.Drop rows with any missing values
df_cleaned = df.dropna()
# Display the cleaned DataFrame
print(df_cleaned)
# 2.Fill missing values with 0
df_filled = df.fillna(0)
# Display the DataFrame with filled values
print(df_filled)
# 3.Fill missing values with the mean of each column
df_filled_mean = df.fillna(df.mean())
# Display the DataFrame with filled values
print(df_filled_mean)

# 4. Calculate summary statistics
# Pandas provides several functions to calculate summary statistics.
# 1.Calculate summary statistics for the DataFrame
summary_stats = df.describe()
print(summary_stats)
# 2.Calculate the sum of column 'slope'
sum_A = df['slope'].sum()
print(f"Sum of column slope:{sum_A}")
# 3.Calculate the mean of column 'slope'
mean_B = df['slope'].mean()
print(f"Mean of column slope: {mean_B}")

