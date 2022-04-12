# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE
```
import numpy as np

import pandas as pd

import seaborn as sns

df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=true)
df.isnull().sum()
df['Age']=df['Age'].fillna(df['Age'].median()) df['Embarked']=df['Embarked'].fillna(df['Embarked'].mode()[0]) df.isnull().sum()
df.boxplot()
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Pclass"],df["Sex"])
pd.crosstab(df["Sex"],df["Survived"])
sns.countplot(x='Survived',data=df)
df.corr()
sns.countplot(x='Pclass',data=df)
df.info()
sns.displot(df["Age"])
sns.displot(df["Fare"])
sns.countplot(x='Pclass',hue="Survived",data=df)
sns.countplot(x='Age',hue='Survived',data=df)
sns.displot(df[df['Survived']==0]["Age"])
sns.heatmap(df.corr(),annot=True)

```


# OUTPUT
![image](pic1.png)
![image](pic2.png)
![image](pic3.png)
![image](pic4.png)
![image](pic5.png)
![image](pic6.png)
![image](pic7.png)
![image](pic8.png)
![image](pic9.png)
![image](pic10.png)
![image](pic11.png)
![image](pic12.png)
![image](pic13.png)
![image](pic14.png)
![image](pic15.png)
![image](pic16.png)
![image](pic17.png)
![image](pic18.png)
![image](pic19.png)
![image](pic20.png)
![image](pic21.png)
![image](pic22.png)

# RESULT
Finally, the given data's were analyzed successfully