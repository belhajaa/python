## numpy

## matplotlib

## pandas
provides two important data structutre : series and dateFrame.

series is like dictionary and provide a number of interesting feature likeperforming arithmetics and access via location

```pyt
from math import sqrt
import pandas as pd
import matplotlib.pyplot as plt

series = pd.Series([10,20,20],['A','B', 'C'])#the second is the index collection
series.name = "my first serie in py"
print(series)

# Access to the series
## Access by the keys
print(series['B'])

## Access by the location
print(series.iloc[2])

#convert to a dict 
print("dict convertion of the serie", dict(series))

#we can add two series content 
s1 = pd.Series([10,20,100],['A','B', 'C'])
s2 = pd.Series([99,60,70],['A','B', 'C'])
print(s1 + s2)

#head and tail function
print(s1.head(2))
print(s2.tail(2))
#apply a function to all the values of the series
def my_squareroot(x):
    return sqrt(x)
print(s1.apply(my_squareroot))

#diffrent sorting type sort_index and sort_values and return the new serie
print(s2.sort_values())
print(s2.sort_index())
#we can impact the same object by adding the inplace param
s2.sort_index(inplace = True)

#print a series is simple with matplotlib
s1.plot()
plt.savefig('output.png')

#export to any data type via the function to_ (to_sql, to_excel, to_jason, To_latex)
s1.to_csv('my_seires.csv')

```
