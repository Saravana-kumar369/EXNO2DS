# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv('/content/titanic_dataset.csv')
print(df.head())
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/5a9461ab-7aa2-4268-b6ff-46a10a982345)
```
df.info()
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/3e68d3c0-c2f2-462b-87ff-054dbc8435e4)
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/6b2ab996-8094-4cc6-8baa-c4d7a27d7985)
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/2e156581-2bb6-4730-a08b-adbc2a9c2b65)
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/dd9afeb7-1aae-42b8-a9f1-c691f8a082c5)
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/0f395f6f-99b1-4de8-aed9-261903ae3364)
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/db5590fc-83b5-4ac7-ac52-6816dbdc2d54)
```
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/db5d87f8-afb8-46a1-8866-4e71a4c7cd29)
```
df.Pclass.unique()
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/211f60ea-72d1-4698-b9bd-bef25cc5167c)
```
df.rename(columns ={'Sex': 'Gender'}, inplace = True)
df
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/7d7bdb86-5748-4c9c-90dc-96094cd14b8c)
```
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=0.7,color="Lightgreen")
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/7d6473d2-a2b7-4d2e-a9f7-530218a8a07a)
```
sns. catplot(x='Survived', hue="Gender",data=df, kind = "count" )
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/e79daaa4-7538-4fc9-8b83-73e953358635)
```
df.boxplot(column="Age", by="Survived")
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/00e9539e-8bb1-4b38-b8a9-b872e9dd4e6a)
```
sns.scatterplot(x=df['Age'],y=df['Fare'])
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/4838f5ad-576c-45fb-bf28-6968b3eeefc7)
```
sns.jointplot(x="Age",y="Fare",data=df)
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/95659236-ef27-4e13-8cfc-29634756560e)
```
fig, ax1= plt.subplots(figsize=(8,5))
pt=sns.boxplot (ax=ax1,x='Pclass',y='Age' ,hue= 'Gender', data=df)
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/dd3cfa1a-502d-4163-b7bd-a06ede59c686)
```
sns. catplot(data=df, col = "Survived",x = "Gender", hue="Pclass", kind = "count" )
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/a29e41b4-50df-44cb-b346-53aad5f612d1)
```
corr=df.corr()
sns.heatmap(corr,annot=True)
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/1f4ebbae-2cce-4842-a634-314ed03eccf3)
```
sns.pairplot(df)
```
![image](https://github.com/Saravana-kumar369/EXNO2DS/assets/117925254/9ddcfac2-4cdf-4ff4-8666-462fe3dbd3c7)




















# RESULT
        <<INCLUDE YOUR RESULT HERE>>
