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
### NumPy array comparison:
```
Note:  np.logical_and(), np.logical_or() and np.logical_not(), the Numpy variants of the and, or and not operators
```
### Looping Data Structures:
1. Dictionary:
```
for key, val in my_dict.items()
```
2. Numpy array:(2d or more dimensional array)
```
for val in np.nditer(my_array)
```
### Random Walk Building
``` Python
import matplotlib.pyplot as plt
import numpy as np
np.random.seed(123)
all_walks = []
for i in range(10) :
    random_walk = [0]
    for x in range(100) :
        step = random_walk[-1]
        dice = np.random.randint(1,7)
        if dice <= 2:
            step = max(0, step - 1)
        elif dice <= 5:
            step = step + 1
        else:
            step = step + np.random.randint(1,7)
        random_walk.append(step)
    all_walks.append(random_walk)

# Convert all_walks to Numpy array: np_aw
np_aw = np.array(all_walks)

# Plot np_aw and show
plt.plot(np_aw)
plt.show()
# Clear the figure
plt.clf()

# Transpose np_aw: np_aw_t
np_aw_t = np.transpose(np_aw)

# Plot np_aw_t and show
plt.plot(np_aw_t)
plt.show()
```

### Lambda Expression with map()
``` Python
# Create a list of strings: spells
spells = ["protego", "accio", "expecto patronum", "legilimens"]

# Use map() to apply a lambda function over spells: shout_spells
shout_spells = map(lambda spell: spell + '!!!', spells)

# Convert shout_spells to a list: shout_spells_list
shout_spells_list = list(shout_spells)

# Convert shout_spells into a list and print it
print(shout_spells_list)

```
### Lambda Expression with filter()
``` Python
# Create a list of strings: fellowship
fellowship = ['frodo', 'samwise', 'merry', 'pippin', 'aragorn', 'boromir', 'legolas', 'gimli', 'gandalf']

# Use filter() to apply a lambda function over fellowship: result
result = filter(lambda member : len(member) > 6, fellowship)

# Convert result to a list: result_list
result_list = list(result)

# Convert result into a list and print it
print(result_list)

```
### Lambda Expression reduce()
he reduce() function is useful for performing some computation on a list and, unlike map() and filter(),
returns a single value as a result. To use reduce(), you must import it from the functools module.
``` Python
# Import reduce from functools
from functools import reduce

# Create a list of strings: stark
stark = ['robb', 'sansa', 'arya', 'brandon', 'rickon']

# Use reduce() to apply a lambda function over stark: result
result = reduce(lambda item1, item2 : item1 + item2, stark)

# Print the result
print(result)

```
``` Python
### Zip
In [1]: avengers = ['hawkeye', 'iron man', 'thor', 'quicksilver'] 
In [2]: names = ['barton', 'stark', 'odinson', 'maximoff'] 
In [3]: z = zip(avengers, names) 
In [4]: print(type(z)) <class 'zip'> 
In [5]: z_list = list(z) 
In [6]: print(z_list) [('hawkeye', 'barton'), ('iron man', 'stark'), ('thor', 'odinson'), ('quicksilver', 'maximoff')
```