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

<img width="929" height="498" alt="image" src="https://github.com/user-attachments/assets/9d880fe2-66de-4040-b96e-d0e758aba0ba" />

# 1.Lineplot:

```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```

<img width="939" height="572" alt="image" src="https://github.com/user-attachments/assets/2b420878-6ee5-42ac-84a8-bc65619687f6" />

# 2.Multi Line Plot:

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

<img width="922" height="641" alt="image" src="https://github.com/user-attachments/assets/7f9e2928-cf86-4095-833d-d06c13545086" />

# TO VISUALIZE RELATIONSHIPS
# 1.Bar Chart:

```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```

<img width="932" height="694" alt="Screenshot 2025-10-23 090440" src="https://github.com/user-attachments/assets/87c31098-aa85-418b-a7e9-71caf01141ca" />

# 2.Scatter Plot:

```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```

<img width="914" height="549" alt="image" src="https://github.com/user-attachments/assets/7efcc457-6bc7-40ce-acfa-9a4229224cfe" />

# 3.Bubble Chart:

```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```

<img width="922" height="543" alt="image" src="https://github.com/user-attachments/assets/738d89eb-ce78-403b-aa18-3d3bc9024171" />

# TO CAPTURE DISTRIBUTIONS
#  1.Histogram

```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="909" height="520" alt="image" src="https://github.com/user-attachments/assets/e7e6e3af-38f4-400e-b420-90929662bbdd" />

#  2.Boxplot

```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```

<img width="931" height="655" alt="image" src="https://github.com/user-attachments/assets/d4565ced-34ba-4848-b137-2893ac882dff" />

#  3.Violin Plot

```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```

<img width="898" height="550" alt="image" src="https://github.com/user-attachments/assets/6ccd8cd3-fc33-49b3-bc90-3e24f8dd679c" />

#  4.Density Plot

```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```

<img width="929" height="653" alt="image" src="https://github.com/user-attachments/assets/38a71bcc-ab57-438c-ba45-f871b83190c6" />

#  5.Heatmap

```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```

<img width="942" height="642" alt="image" src="https://github.com/user-attachments/assets/df6bc39e-8dcc-47d9-9f11-e9a1ed4b3494" />

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
