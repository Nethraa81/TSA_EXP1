# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 19.08.2025

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
from matplotlib import pyplot as plt
import pandas as pd
df = pd.read_csv("complete_dataset.csv", encoding="ISO-8859-1")
df["date"] = pd.to_datetime(df["date"])
df.set_index("date", inplace=True)
df_resampled = df["demand"].resample("D").interpolate()
plt.figure(figsize=(10, 6))
df_resampled.plot(kind="line", label="Electricity Demand", color="black")
plt.title("Daily Electricity Demand Over Time")
plt.xlabel("Date")
plt.ylabel("Demand")
plt.legend()
plt.grid(True)
plt.show()
```

# OUTPUT:
<img width="1020" height="537" alt="image" src="https://github.com/user-attachments/assets/bd75b48f-15ff-413a-87c0-73b04e04e2ef" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
