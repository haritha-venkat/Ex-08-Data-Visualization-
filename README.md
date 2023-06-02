# Ex-08-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
```python
name:harithashree.V
reg.no.:212222230046

#Reading the given dataset
import pandas as pd
df=pd.read_csv("Superstore.csv",encoding='unicode_escape')
df.head()
#Data Visualization using Seaborn
import seaborn as sns
from matplotlib import pyplot as plt
#1.Line Plot
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
#2.Scatterplot
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
#3.Boxplot
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
#4.Violin Plot
sns.violinplot(x="Profit",data=df)
#5.Barplot
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
#6.Pointplot
sns.pointplot(x=df["Quantity"],y=df["Discount"])
#7.Count plot
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
#8.Histogram
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
#9.KDE Plot
sns.kdeplot(x="Profit", data = df,hue='Category')
#Data Visualization Using MatPlotlib
#1.Plot
plt.plot(df['Category'], df['Sales'])
plt.show()
#2.Heatmap
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
#3.Piechart
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()
df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
labels.append(i)
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
#4.Histogram
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
#5.Bargraph
plt.bar(df.index,df['Category'])
plt.show()
#6.Scatterplot
OUPUT
Reading the given dataset
## Data Visualization Using Seaborn: ### 1.Line Plot
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show()
#7.Boxplot
plt.boxplot(x="Sales",data=df)
plt.show()
```
## OUPUT:

## reading the given dataset:
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/884a7f52-d871-4b6a-95e4-8c7e25da2316)
## Data Visualization Using Seaborn
## 1.Line Plot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/37294936-c7eb-431f-98d2-6ee4ad952e01)
## scatter plot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/5314cfe0-0bf6-4552-a444-07f1bb752ef8)
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/5ebb60eb-6517-4af6-a34b-ea7321ae3464)

## 3.Boxplot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/cb520522-6b03-4abd-a98a-52f4f5c5de8a)

Violin Plot

![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/1de30b8b-5e2d-4953-a464-bab138d6c947)

5.Barplot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/d25b45fa-9138-47b0-af5b-f50c0d98d69d)


pointplot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/fe41c32b-ea43-449e-8116-eade20a09cda)


Count plot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/ffa62019-c4c4-4929-a37f-6539bc52497e)


Histogram
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/a8f5e716-1167-4e17-a555-49a3d7837997)

DE plot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/ff5460da-6413-4268-b1f1-02ab208af0ab)


Data Visualization Using Matplotlib:
Plot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/d9be71f6-5166-48b1-9353-1cb7ec7b197a)


Heatmap
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/6aa81c68-892b-4595-a03a-7419e97e92f3)


Piechart
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/5132206e-b265-425e-a0d9-fa434c97929e)


![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/fee657d5-877a-4278-a9c2-239961bf0c71)


Histogram
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/e40a636a-9193-4128-8a41-e92a31d24720)


Bargraph

![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/57551e7a-bf45-42e9-a198-68c2e4a0b303)

Scatterplot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/3017c212-8ac4-4269-82f8-a631862178a0)


Boxplot
![image](https://github.com/haritha-venkat/Ex-08-Data-Visualization-/assets/121285701/eece1431-7778-40ce-a816-6d6bccf1c5b1)


RESULT

Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file
