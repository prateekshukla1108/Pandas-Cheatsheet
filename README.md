
### Importing Pandas
- **`import pandas as pd`**: Imports the Pandas library and allows you to use it with the alias `pd`.

### Creating DataFrames
- **`pd.DataFrame(data)`**: Creates a DataFrame from a dictionary or other data structures.
- **`pd.read_csv('file.csv')`**: Reads data from a CSV file into a DataFrame.
- **`pd.read_excel('file.xlsx')`**: Reads data from an Excel file into a DataFrame.
- **`pd.DataFrame(array, columns=['...'])`**: Creates a DataFrame from a NumPy array with specified column names.

### Basic DataFrame Operations
- **`df.head()`**: Displays the first 5 rows of the DataFrame.
- **`df.tail()`**: Displays the last 5 rows of the DataFrame.
- **`df.info()`**: Provides a summary of the DataFrame, including data types and number of entries.
- **`df.describe()`**: Generates descriptive statistics for numerical columns.
- **`df.columns`**: Returns the names of the DataFrame's columns.
- **`df['Column1']`**: Selects a specific column from the DataFrame.
- **`df[['Column1', 'Column2']]`**: Selects multiple columns.
- **`df.iloc[index]`**: Selects rows by integer index.
- **`df[df['Column1'] > 1]`**: Filters rows based on a condition.

### Modifying DataFrames
- **`df['NewColumn'] = ...`**: Adds a new column with computed values.
- **`df.drop('ColumnName', axis=1)`**: Removes a specified column.
- **`df.rename(columns={'old_name': 'new_name'})`**: Renames columns.
- **`df.set_index('Column')`**: Sets a specified column as the DataFrame index.
- **`df.reset_index()`**: Resets the index to default integer values.

### Handling Missing Data
- **`df.isnull().sum()`**: Returns the count of missing values in each column.
- **`df.dropna()`**: Removes rows with missing values.
- **`df.fillna(value)`**: Replaces missing values with a specified value.

### Data Aggregation and Grouping
- **`df.groupby('Column')`**: Groups the DataFrame by the specified column.
- **`mean()`**: Calculates the mean of grouped data.
- **`agg({'Column': ['func1', 'func2']})`**: Applies multiple aggregation functions to grouped data.

### Merging and Joining
- **`pd.merge(df1, df2, on='key')`**: Merges two DataFrames on a specified key.
- **`pd.concat([df1, df2], axis=0)`**: Concatenates multiple DataFrames either vertically (rows) or horizontally (columns).

### Time Series
- **`pd.to_datetime(df['date_column'])`**: Converts a string column to datetime format.
- **`df.set_index('date')`**: Sets the datetime column as the index for time series analysis.
- **`resample('M').mean()`**: Resamples data by specified frequency (e.g., monthly) and computes the mean.

### Visualization
- **`df['Column'].plot()`**: Plots basic line graphs for a specified column.
- **`df['Column'].hist(bins=20)`**: Creates a histogram for visualizing the distribution of a column.
- **`df.plot.scatter(x='col_x', y='col_y')`**: Generates a scatter plot with specified x and y columns.

### Exporting DataFrames
- **`df.to_csv('output.csv', index=False)`**: Exports the DataFrame to a CSV file.
- **`df.to_excel('output.xlsx', index=False)`**: Exports the DataFrame to an Excel file.
- **`df.to_json('output.json')`**: Exports the DataFrame to a JSON file.

