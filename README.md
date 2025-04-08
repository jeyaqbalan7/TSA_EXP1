## Date:

## Aim:
To Develop a python program to Plot a time series data of Rainfall rate

## ALGORITHM:
1.Import the required packages like pandas and matplot

2.Read the dataset using the pandas

3.Plot the data according to need and can be altered monthly, or yearly.

4.Display the graph.

## Program:
```
import pandas as pd
import matplotlib.pyplot as plt
file_path = 'rainfall.csv'  # Replace with your file path
data = pd.read_csv('rainfall.csv')
data['date'] = pd.to_datetime(data['date']) # Changed 'Date' to 'date' to match column name
data.set_index('date', inplace=True)
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['rainfall'], label='rainfall', color='blue') # Changed 'rainfall Today' to 'rainfall' assuming it's the correct column name
plt.title('rainfall Today Over Time')
plt.xlabel('Date')
plt.ylabel('rainfall')
plt.grid(True)
plt.legend()
plt.show()
data.sample(100)
```

## Output:
![image](https://github.com/user-attachments/assets/512679c5-0a6e-4f9a-b402-617c610d2bc6)

## Result:
Thus we have created the python code for plotting the time series of given data.
