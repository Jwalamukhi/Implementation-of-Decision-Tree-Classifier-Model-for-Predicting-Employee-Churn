# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5. Find the accuracy of the model and predict the required values by importing the required module from sklearn.


## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Jwalamukhi S
RegisterNumber: 212223040079

import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evalution","number_project","average_montly_hours","time_spend_company","work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
Data.head():

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/1ff6d829-2b8f-4fbb-bd47-1c2ad30e9afd)


Data.info():
![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/691cb017-0dc8-4770-80ae-1fb21f85703f)

isnull() and sum():

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/58ceb990-55f3-4627-acc0-6de668083cff)


Data Value Counts():

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/8f8667ad-8fca-444a-9147-c0b2edfc5f1c)


Data.head() for salary:

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/0fcf4431-5b28-4dc9-af77-89ec5349e76b)


x.head:
![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/3fad299a-cc3f-4067-869c-bf1a7acb0a42)


Accuracy Value:

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/f7a422ea-6fe9-4ae6-8b02-80a50063bdf8)


Data Prediction:
![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/d97e3136-2c84-4940-8aac-36114c4caaac)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
