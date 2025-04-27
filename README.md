# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```

```
x = [1,2,3,4,5,]
y1 = [3,5,2,6,1]
y2 = [1,6,4,3,8]
y3 = [5,2,7,1,4]
sns.lineplot(x=x,y=y1,label="line 1")
sns.lineplot(x=x,y=y2,label="line 2")
sns.lineplot(x=x,y=y3,label="line 3")
plt.xlabel('X Label')
plt.ylabel('Y Label')
plt.title('Multi-Line Plot')
plt.legend()
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175344.png>)
```
tips = sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue = 'sex', data=tips,palette = 'Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175354.png>)
```
sns.scatterplot(x='total_bill',y='tip', hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs Tip Amount')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175405.png>)
```
np.random.seed(0)
marks = np.random.normal(loc=70,scale=10,size=100)
marks
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175412.png>)
```
sns.histplot(data=marks, bins=10, kde=True, stat='count', cumulative=False, multiple='stack', element='bars', palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of Student Marks')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175518.png>)
```
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Box Plot of Total Bill by Day and Gender')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175524.png>)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
            whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175531.png>)
```
sns.violinplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=3, width = 0.7, palette='Set3', inner ='quartile')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Violin Plot of Total Bill by Day and Smoker Status')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175536.png>)
```
sns.set(style='whitegrid')
sns.violinplot(x='tip', y='day',data=tips)
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175542.png>)
```
plt.figure(figsize=(11, 11))
plt.subplot(3,1,1)
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='fill', linewidth=2, palette='Set2', alpha=0.8)
plt.subplot(3,1,2)
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='layer', linewidth=2, palette='Set2', alpha=0.8)
plt.subplot(3,1,3)
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='stack', linewidth=2, palette='Set2', alpha=0.8)
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175554.png>)
```
data = np.random.randint(low=1, high=100, size=(10,10))
print("Data to be plotted")
print(data)
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175559.png>)
```
plt.figure(figsize=(12,5))
plt.subplot(1,2,1)
sns.heatmap(data=data)
plt.subplot(1,2,2)
sns.heatmap(data=data, annot=True)
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175614.png>)
```
numeric_cols = tips.select_dtypes(include=np.number).columns
corr = tips[numeric_cols].corr()
sns.heatmap(corr,annot=True, cmap='plasma', linewidths=0.5)
```
![alt text](<Output Screenshots/Screenshot 2025-04-27 175621.png>)

# Result:
Data visualization through Seaborn was completed and the results have been successfully verified. 
