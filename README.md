# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 04/03/25

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
import pandas as pd
import matplotlib.pyplot as plt
file_path = 'lung_disease_data.csv'
data = pd.read_csv(file_path)
data = data.sort_values(by='Age')
data['Age'] = pd.to_numeric(data['Age'], errors='coerce')
data = data.dropna(subset=['Age', 'Lung Capacity'])
data = data.head(100)
data.set_index('Age', inplace=True)
plt.figure(figsize=(10, 8))
plt.plot(data.index, data['Lung Capacity'], label='Lung Capacity', color='blue')
plt.title('Lung Capacity Over Age')
plt.xlabel('Age')
plt.ylabel('Lung Capacity')
plt.grid(True)
plt.legend()
plt.show()
```

# OUTPUT:

![image](https://github.com/user-attachments/assets/c99dcea7-2123-4312-aa0c-5e71d1f4fd3f)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
