# Titanic-Data-Analysis
Exploratory Data Analysis using Univariate 
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df = pd.read_csv('Titanic.csv')
df.sample(10)

1. Categorical Data
a. Countplot
sns.countplot(df['Pclass'])
sns.countplot(df['Survived'])
df['Survived'].value_counts().plot(kind='bar')

b. PieChart
df['Embarked'].value_counts().plot(kind='pie',autopct='%.2f%%')


2. Numerical Data
a. Histogram
plt.hist(df['Age'],bins=50)

b. Distplot
sns.distplot(df['Age'])

c. Box Plot
sns.boxplot(df['Age'])

df['Age'].std() #used to find the values of standard deviation
