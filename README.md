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
import seaborn as sns 
import matplotlib.pyplot as plt 
df=pd.read_csv("titanic_dataset.csv") 
df.head()
```
<img width="1215" height="190" alt="image" src="https://github.com/user-attachments/assets/f7a6ff96-a3d6-4b39-95ca-f3b5063ca20e" />

```
x=[1,2,3,4,5] 
y=[3,6,2,7,1] 
sns.lineplot(x=x,y=y) 
plt.title('Line Plot')
```
<img width="672" height="576" alt="image" src="https://github.com/user-attachments/assets/136b4af5-4447-4fa0-9fe0-d97bac29b503" />

```
x=[1,2,3,4,5] 
y1=[3,5,2,6,1] 
y2=[1,6,4,3,8] 
y3=[5,2,7,1,4] 
sns.lineplot(x=x,y=y1) 
sns.lineplot(x=x,y=y2) 
sns.lineplot(x=x,y=y3) 
plt.title('Multi Line Plot')
```
<img width="673" height="572" alt="image" src="https://github.com/user-attachments/assets/72d699e1-e9c8-4616-ba7f-e41643283241" />

```
plt.figure(figsize=(8,5)) 
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow') 
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="870" height="613" alt="image" src="https://github.com/user-attachments/assets/b88ec111-0444-4960-b7fc-f689b6164e1b" />

```
sns.scatterplot(x="Age", y="Fare", data=df) 
plt.title('Scatterplot of Age vs Fare') 
plt.show()
```
<img width="725" height="557" alt="image" src="https://github.com/user-attachments/assets/d32f3800-1dfe-4bd1-af0a-46affa7601ea" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200)) 
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class') 
plt.show()
```
<img width="725" height="557" alt="image" src="https://github.com/user-attachments/assets/028cad39-118c-4695-8718-8f7f84c6d071" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="751" height="581" alt="image" src="https://github.com/user-attachments/assets/0371a48c-9b09-454f-ab28-a834006438ce" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow') 
plt.title("Age By Passenger Class")
```
<img width="732" height="601" alt="image" src="https://github.com/user-attachments/assets/b880e877-5338-4fcc-a202-df7d634c2f11" />

```
sns.violinplot(x="Pclass", y="Fare", data=df) 
plt.title('Violin Plot of Fare by Passenger Class') 
plt.show()
```
<img width="737" height="557" alt="image" src="https://github.com/user-attachments/assets/27ca8c80-fd90-4c3a-ab65-7b46ff2c0bfc" />

```
sns.kdeplot(data=df['Age'], shade=True) 
plt.title('Density Plot of Passenger Ages') 
plt.show()
```
<img width="752" height="563" alt="image" src="https://github.com/user-attachments/assets/34d75d65-7f47-44e9-9e64-9ee7bcd060c7" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64']) 
corr_matrix = numeric_df.corr() 
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm') 
plt.title('Heatmap of Titanic Dataset') 
plt.show()
```
<img width="768" height="633" alt="image" src="https://github.com/user-attachments/assets/1cbc2f35-6ab3-4a03-84c3-9cf2f28052e8" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.
