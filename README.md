# data-camp
This repository contains python &amp; machine learning materials, solutions. These courses has taken from the datacamp

## **NumPy:**
NumPy arrays are a bit like Python lists, but still very much different at the same time.Here all the elements should be same type(```Homogeneous elements```)
```
List doesn't support arithmetic manipulations like double the list, *,%,/..etc. so Numpy came into existence
```
## **Pandas:**
Pandas is an open source library, providing high-performance, easy-to-use data structures and data analysis tools for Python. 
Sounds promising! The DataFrame is one of Pandas' most important data structures. 
It's basically a way to store tabular data where you can label the rows and the columns.
One way to build a DataFrame is from a dictionary.
```
Numpy supports only for homogeneous elements.So pandas came, it can have heterogeneous elements. 
```
### DataFrame:(pandas)
Putting data in a dictionary and then building a DataFrame works, but it's not very efficient. 
What if you're dealing with millions of observations? In those cases, the data is typically available as files with a regular structure. 
One of those file types is the CSV file, which is short for "comma-separated values".
1. Column Access:
dataframe[["column_name"]]
2. Row Access:
	* **loc-labled access**
	dataframe.loc[["index_name/row name"]]
	* **iloc-index access**
	dataframe.iloc[["index_number"]]
```
Note:  np.logical_and(), np.logical_or() and np.logical_not(), the Numpy variants of the and, or and not operators
```