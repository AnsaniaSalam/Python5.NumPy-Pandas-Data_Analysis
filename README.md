# Data Analysis using NumPy and Pandas

This Jupyter notebook contains hands-on Python exercises with NumPy and Pandas. It demonstrates how to analyse temperature data with arrays, work with labelled marks in a Series, and explore and modify sales transactions in a DataFrame.

## Concepts Used

### NumPy Arrays
`np.array()` turns a list into an array. A list of lists creates a 2D array, where each row is a week and each column is a day.

### Array Properties
`shape`, `dtype` and `size` show the dimensions, data type and total number of elements of an array.

### Vectorised Operations
An operation on an array is applied to every element at once, with no loop needed. It is used here to convert Celsius to Fahrenheit with `(C * 9/5) + 32`.

### Array Statistics
`max()`, `min()` and `mean()` return the highest, lowest and average value of an array.

### Array Indexing & Slicing
`[:3]` gives the first three days, `[-2:]` the last two, and `[2:5]` the middle three. In 2D, `temperatures[:, -2:]` takes the weekend columns from every row.

### Pandas Series
A one-dimensional labelled array. Custom index labels like `Rank1` to `Rank5` let each mark be found by name.

### loc and iloc
`loc` selects by label and includes the last label in a slice. `iloc` selects by position, starting from `0`.

### Boolean Masking
A condition such as `marks > 90` gives True or False for each item. Passing the mask back into the Series keeps only the True rows.

### Modifying a Series
Assign to a label to change a value, `drop()` to remove an entry, and divide the Series by a number to apply it to every value (marks to CGPA).

### Pandas DataFrame
A table of rows and columns, created here from a dictionary of lists.

### Data Exploration
`head()`, `tail()`, `shape`, `columns` and `dtypes` give a quick overview of the data. `iloc[:, -3:]` selects the last three columns.

### Column Selection & Filtering
`df[['ProductCategory', 'Amount']]` selects columns. Conditions joined with `&` filter rows, e.g. Region is North and Amount is above 200.

### value_counts() and unique()
`value_counts()` counts how often each value appears. `unique()` lists each distinct value once.

### groupby()
Splits the rows into groups and calculates a value for each group, e.g. the mean amount per region.

### Modifying a DataFrame
`loc` changes a single value, a new column is created by assigning to a new name (10% discount), and `drop()` removes a row or a column.

### print() Function
Displays labelled output for readability.

## Running the Code

Open the notebook in Jupyter Notebook or JupyterLab and run the cells in order, starting with the setup cell that imports NumPy and Pandas. Both libraries come installed with Anaconda. Otherwise, install them with:

```bash
pip install numpy pandas
```

To run it from a terminal instead, execute the notebook with:

```bash
jupyter nbconvert --to notebook --execute "Python5.NumPy_Pandas_Data_Analysis.ipynb"
```
