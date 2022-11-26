# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries .
2. Read the data frame using pandas.
3. Get the information regarding the null values present in the dataframe.
4. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5. Determine training and test data set.
6. Apply decision tree regression on to the dataframe.
7. Get the values of Mean square error, r2 and data prediction.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: J.DEEPIKA
RegisterNumber: 212221230016

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
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
*/
```

## Output:


![22222222](https://user-images.githubusercontent.com/94747031/199081129-37ef09de-6a2d-4bdd-a766-7440d677c6a0.png)

![1111111](https://user-images.githubusercontent.com/94747031/199081143-7ce45a9f-2b29-44d3-a3a9-abb1dcf48d14.png)

![88888888](https://user-images.githubusercontent.com/94747031/199081161-7b4c28de-bc56-4359-988c-b8ba0ec1eb25.png)


![66666666](https://user-images.githubusercontent.com/94747031/199081175-dce0ebc1-b28a-4592-bedc-d33eaca49b36.png)

![555555555](https://user-images.githubusercontent.com/94747031/199081195-c4ea2c15-8a99-4c22-a5a3-43dc61381144.png)

![4444444](https://user-images.githubusercontent.com/94747031/199081200-062e4219-668a-4abb-a1f9-77c32101ec49.png)

![33333333](https://user-images.githubusercontent.com/94747031/199081208-73e43bac-352f-4ea1-866a-b93c8fef94ae.png)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
