# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import pandas and read the csv file.
2.Encoding the data and Import Decision tree classifier.
3.Fit the data in the model.
4.Find the MSE , r2 and the Predicted


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: SIBIRAJ E
RegisterNumber:  212223080052
*/

import pandas as pd
df=pd.read_csv("CSVs/Salary.csv")
df.head(10)
df.info()
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df['Position']=le.fit_transform(df['Position'])
df.head(10)
x=df[['Position','Level']]
y=df['Salary']
from sklearn.model_selection import train_test_split as tts
Xtrain,Xtest,Ytrain,Ytest=tts(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(Xtrain,Ytrain)
Ypred=dt.predict(Xtest)
from sklearn import metrics
mse=metrics.mean_squared_error(Ytest,Ypred)
mse
r2=metrics.r2_score(Ytest,Ypred)
r2
dt.predict([[5,6]])
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)

![image](https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/160568857/1ee6cb0e-86b2-4636-b1f6-b38a85dc8826)

![image](https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/160568857/58772351-7b62-424a-a7e4-f4b210f73204)

![image](https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/160568857/a0b23421-cfef-4860-b510-077937e9f654)

![image](https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/160568857/bfab0566-5721-4624-9c9c-0129b0065287)

![image](https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/160568857/4a733c84-732c-4777-9dee-29850bb0e93a)

![image](https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/160568857/0e64c271-7d81-4510-a2ec-b23841119eee)

![image](https://github.com/AkilaMohan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/160568857/fd0f6088-7642-4725-b70b-5c1a5da60b19)








## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
