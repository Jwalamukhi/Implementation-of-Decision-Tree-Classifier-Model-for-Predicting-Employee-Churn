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

### Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
### Developed by: Jwalamukhi S
### RegisterNumber: 212223040079
```
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

```

## Output:
Data.head():

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/471ec174-9411-43f1-8cfe-f70f37616849)



Data.info():

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/0a7c01e9-62eb-4e4e-a292-c42580a06b11)

isnull() and sum():

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/98f6912a-2a70-4dee-b2e1-3e5a48982f4e)


Data Value Counts():

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/89876ef2-1340-49b9-8e42-ef16bb8bfc87)


Data.head() for salary:

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/a82f0207-6316-45cb-a38d-4a6b58595425)


x.head:

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/3f2170ed-3e92-4669-adfb-3e783e1769d4)


Accuracy Value:

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/df63131c-f73d-492a-be30-dac9bb064ef7)



Data Prediction:

![image](https://github.com/Jwalamukhi/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/145953628/bc26f313-ebd2-4e44-b37f-9249b9624d63)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
