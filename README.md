# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## Aim:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. Calculate Mean square error,data prediction and r2.
5. Print the obtained values.

## Program:

Developed by: Sneha Basyal M

RegisterNumber: 212222240101

```
import pandas as pd
data=pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

## Output:

## data.head()
![Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee](ML71.png)
<br>

## data.info()
![Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee](ML72.png)
<br>

## isnull() and sum() function
![Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee](ML73.png)
<br>

## data.head() for Position
![Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee](ML74.png)
<br>

## MSE value
![Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee](ML75.png)
<br>

## R2 value
![Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee](ML76.png)
<br>

## Prediction value
![Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee](ML77.png)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
