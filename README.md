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
import pandas as pd
import matplotlib.pyplot as plt

# Load dataset (adjust path if needed)
df = pd.read_csv("openpowerlifting.csv")

# Group by MeetID and take average of TotalKg
df_grouped = df.groupby("MeetID")["TotalKg"].mean()

# Plot as line chart
df_grouped.plot(kind='line', color='black', label='Average TotalKg per Meet')
plt.title("Average Powerlifting Total over Competitions")
plt.xlabel("Meet ID (Competition)")
plt.ylabel("Average Total (Kg)")
plt.legend()
plt.grid(True)
plt.show()




# OUTPUT:


<img width="1920" height="1140" alt="Screenshot 2025-08-19 083923" src="https://github.com/user-attachments/assets/2272d03e-0704-43bb-ad97-a68d4921757d" />




# RESULT:
Thus we have created the python code for plotting the time series of given data.
