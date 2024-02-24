# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 16-02-2024

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
## Population:

```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df_filtered = df["2000":"2023"]
annual_mean = df_filtered.resample('Y').mean()
mean = annual_mean.plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population (in Thousands)")
plt.title("Average Annual Population (2000-2023)")
plt.show()
```
# Market Price:
```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
# Temperature:
```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```


# OUTPUT:
## Population:
![w](https://github.com/BHUVANESHWAR-BHUVIOP/TSA_EXP1/assets/94155099/4ab322b9-76fe-4101-bd99-0bf98f6b65a0)

# Market Price:
![ww](https://github.com/BHUVANESHWAR-BHUVIOP/TSA_EXP1/assets/94155099/e1606337-afcf-471e-a652-b505da1d06f9)


# Temperature:
![www](https://github.com/BHUVANESHWAR-BHUVIOP/TSA_EXP1/assets/94155099/8f87410c-0769-4eba-b265-fe8b9fa64d59)



# RESULT:
Thus we have created the Python code for plotting the time series of given data.
