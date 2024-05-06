# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import pandas library to read csv or excel file.
2. Import LabelEncoder using sklearn.preprocessing library.
3. Transform the data's using LabelEncoder.
4. Import decision tree classifier from sklearn.tree library to predict the values.
5. Find accuracy.
6. Predict the values.
7. End of the program.

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:  VEMBARASAN P
RegisterNumber:  212223220123

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
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
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

## HEAD:

![image](https://user-images.githubusercontent.com/98681990/174658785-dbeb43ad-725b-44e9-88d1-1971e6b605fd.png)

## INFO:

![image](https://user-images.githubusercontent.com/98681990/174659151-628fca92-47fa-4abc-ab4a-2aa82452d9f3.png)

## ISNULL:

![image](https://user-images.githubusercontent.com/98681990/174659210-dfa89fd7-a2ac-45ce-b1ed-2a6e556b6b91.png)

## LEFT:

![image](https://user-images.githubusercontent.com/98681990/174659236-28bfb25c-e1e1-4906-8fc1-63c48b85ac2a.png)

## HEAD USING LABELENCODER:

![image](https://user-images.githubusercontent.com/98681990/174659261-6ae628e0-828e-4c2e-95ba-602b70d14b36.png)

## ACCURACY:

![image](https://user-images.githubusercontent.com/98681990/174659305-84fd74dd-13ee-4ef2-b0ef-e540c59a6354.png)

## PREDICT:

![image](https://user-images.githubusercontent.com/98681990/174659331-e6df8723-51b2-4988-9fbe-9cfd012cadc8.png)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
