# Summary and Functions Used in Traffic Accidents Data Analysis

## Summary

You are working with a pandas DataFrame, `df`, which contains traffic accident data read from the CSV file `traffic_accidents.csv`. The analysis includes data exploration, cleaning, and visualization. Below are the key tasks performed:

- **Reading the Data**: You loaded the CSV data into a pandas DataFrame.
- **Data Exploration**: You previewed the data using methods like `head()`, `tail()`, and `sample()`, and checked the shape of the DataFrame.
- **Renaming Columns**: Columns were renamed using the `rename()` method for clarity.
- **Missing Data Handling**: You handled missing data using `fillna()`, `dropna()`, and checked for null values with `isnull()`.
- **Descriptive Statistics**: Summary statistics for numerical and categorical data were obtained using `describe()`.
- **Plotting**: Various plots were generated to visualize the data, particularly the "num_units" column.

## Functions/Methods Used

### 1. **Reading Data**
- `pd.read_csv("traffic_accidents.csv")`: Reads a CSV file into a pandas DataFrame.

### 2. **Previewing Data**
- `df.head(n)`: Returns the first `n` rows of the DataFrame (default is 5).
- `df.tail(n)`: Returns the last `n` rows of the DataFrame.
- `df.sample(n)`: Returns a random sample of `n` rows from the DataFrame.
- `df.shape`: Returns the shape (number of rows and columns) of the DataFrame.

### 3. **Renaming Columns**
- `df.rename(columns={})`: Renames columns in the DataFrame. You should assign the result back to `df` or use `inplace=True`.

### 4. **Missing Data Handling**
- `df.isnull().sum()`: Checks for missing values and returns the count of missing values in each column.
- `df.fillna(value)`: Fills missing values with a specified value (`value`). Use `inplace=True` to modify the DataFrame directly or assign the result back to `df`.
- `df.dropna()`: Drops rows with missing values.
- `df[df["column"].isnull()]`: Filters rows where a particular column contains missing values.

### 5. **Descriptive Statistics**
- `df.describe()`: Provides summary statistics (mean, std, min, 25%, 50%, 75%, max) for numerical columns.
- `df.describe(include="all")`: Provides summary statistics for both numerical and categorical columns.
- `df["column"].mean()`: Computes the mean (average) of a column.
- `df["column"].median()`: Computes the median (middle value) of a column.
- `df["column"].mode()`: Computes the mode (most frequent value) of a column.
- `df["column"].std()`: Computes the standard deviation of a column.

### 6. **Plotting**
- `df["column"].plot(kind="line")`: Plots the data of a column as a line plot.
- `df["column"].value_counts().plot(kind="bar")`: Creates a bar plot of the frequency of unique values in the column.
- `df["column"].value_counts().plot(kind="pie")`: Creates a pie chart of the frequency of unique values in the column.
- `df["column"].value_counts().plot(kind="hist")`: Plots a histogram of the frequency of unique values in the column.

### 7. **Grouping and Aggregating**
- `df.groupby("column").describe()`: Groups the DataFrame by a specified column and computes summary statistics for each group.

### 8. **Duplicates**
- `df.duplicated()`: Checks if there are any duplicate rows in the DataFrame (returns a boolean Series).

## Points to Consider
- Ensure you use `inplace=True` or reassign the result when applying methods like `fillna()`, `dropna()`, and `rename()`.
- When handling missing values, use `fillna()` to replace missing data or `dropna()` to remove rows with missing values.
- You used functions like `mean()`, `median()`, `mode()`, and `std()` to calculate key summary statis
