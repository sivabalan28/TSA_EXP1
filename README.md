# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

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
```
SIVABALAN S
212222240100
```
```python
import pandas as pd
import matplotlib.pyplot as plt

data=pd.read_csv("/content/Time-Series Analysis Dataset.csv")
data['datetime_local'] = pd.to_datetime(data['datetime_local'], format='%d-%m-%Y %H:%M')
data.set_index('datetime_local',inplace=True)

plt.figure(figsize=(10,6))
plt.plot(data.index,data['temperature'],label='Temperature Today',color='green')
plt.title('Temperature Today')
plt.xlabel('Date')
plt.ylabel('Temperature')
plt.legend()
```

# OUTPUT:

![Screenshot 2025-03-04 142805](https://github.com/user-attachments/assets/04dd1370-8db8-431d-b644-371702824f32)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
