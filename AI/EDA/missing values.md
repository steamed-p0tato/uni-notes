
## **missing values handling** 

**==pandas cheat sheet==**

---
1. **Handling Missing Values:**
    
    - `df.isnull()` or `df.isna()`: Check for missing values in the DataFrame.
    - `df.dropna()`: Drop rows containing missing values.
    - `df.fillna(value)`: Fill missing values with a specified value.
    - `df.interpolate()`: Interpolate missing values.
2. **Removing Duplicates:**
    
    - `df.duplicated()`: Identify duplicate rows.
    - `df.drop_duplicates()`: Remove duplicate rows.
3. **Changing Data Types:**
    
    - `df.astype()`: Convert the data type of a column.
    - `pd.to_numeric()`, `pd.to_datetime()`, `pd.to_timedelta()`: Convert specific columns to numeric, datetime, or timedelta types.
4. **Renaming Columns:**
    
    - `df.rename(columns={'old_name': 'new_name'})`: Rename specific columns.
5. **Handling Strings:**
    
    - `str.strip()`, `str.lower()`, `str.upper()`: Clean and normalize string data.
    - `str.contains()`: Check for the presence of a substring.
6. **Filtering and Subsetting:**
    
    - `df.loc[]` or `df.iloc[]`: Select specific rows or columns based on labels or integer location.
    - `df.query()`: Perform a query to filter rows based on a condition.
7. **Handling Outliers:**
    
    - Use statistical methods like `mean`, `median`, and `std` to identify and handle outliers.
8. **Applying Functions:**
    
    - `df.apply()`: Apply a function along the axis of the DataFrame.
9. **Sorting Data:**
    
    - `df.sort_values()`: Sort the DataFrame based on specific columns.
10. **Handling Categorical Data:**
    
    - `pd.get_dummies()`: Create dummy variables for categorical columns.
    - `df.astype('category')`: Convert a column to a categorical type.`


#### imputation 

#### *univariate*
- numerical 1.mean / median
			2.random value
			3.end of distribution
- categorized 1.mode
			  2.missing vals
#### *multivariate*
- knn of imputer
- iterative imputer


## regression
