# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Bharath D
RegisterNumber: 212224240025
*/
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
R2 score:  0.48611111111111116


dt.predict([[5,6]])
```
## Output:
<img width="1030" height="314" alt="image" src="https://github.com/user-attachments/assets/f9e6ff51-395e-449b-826f-e86d4e6a349a" />
<img width="495" height="239" alt="image" src="https://github.com/user-attachments/assets/b12146de-fdfe-4cef-b78d-02ef3b3702e9" />
<img width="866" height="161" alt="image" src="https://github.com/user-attachments/assets/17c0f8d7-e46f-441c-9b47-b23b86057665" />
<img width="398" height="36" alt="image" src="https://github.com/user-attachments/assets/9c6978fd-12ac-446c-963b-d4fcbe2d7720" />
<img width="244" height="38" alt="image" src="https://github.com/user-attachments/assets/d6d2add5-04d1-451f-878b-feb61a36df44" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
