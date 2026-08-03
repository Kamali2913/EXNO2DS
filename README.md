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

## CODING AND OUTPUT
```
  import pandas as pd
df=pd.read_csv("C:/Users/acer/Downloads/titanic_dataset.csv")
print(df)
```
![alt text](image.png)
```
df.info()
```
![alt text](image-1.png)
```
df.describe()
```
![alt text](image-2.png)
```
df.shape
```
![alt text](image-3.png)
```
df.dtypes
```
![alt text](image-4.png)
```
df["Survived"].value_counts()
```
![alt text](image-5.png)
```
df.nunique()
```
![alt text](image-6.png)
```
import seaborn as sns
sns.countplot(data=df,x="Survived")
```
![alt text](image-7.png)
```
sns.boxplot(data=df,x="Survived")
```
![alt text](image-8.png)
```
sns.boxplot(data=df,x="Age")
```
![alt text](image-9.png)
```
sns.histplot(data=df,x="Age")
```
![alt text](image-10.png)
```
df.rename(columns={'Sex' : 'Gender'},inplace=True)
print(df)
```
![alt text](image-11.png)
```
sns.catplot(x='Survived',hue="Gender",data=df,kind='count')
```
![alt text](image-12.png)
```
df.boxplot(column="Age",by="Survived")
```
![alt text](image-13.png)
```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```
![alt text](image-14.png)
```
sns.boxplot(x=df["Age"],y=df["Fare"])
```
![alt text](image-15.png)
```
sns.barplot(x=df["Age"],y=df["Fare"])
```
![alt text](image-16.png)
```
sns.barplot(x=df["Survived"],y=df["Fare"])
```
![alt text](image-17.png)
```
sns.boxplot(x="Pclass",y="Age",hue="Gender",data=df)
```
![alt text](image-18.png)
```
sns.catplot(col='Survived',x="Gender",hue="Pclass",data=df,kind='count')
```
![alt text](image-19.png)
```
sns.heatmap(df.corr())
```
![alt text](image-20.png)
```
sns.heatmap(df.corr(),annot=True)
```
![alt text](image-21.png)

# RESULT
          Data analysis was completed successfully
