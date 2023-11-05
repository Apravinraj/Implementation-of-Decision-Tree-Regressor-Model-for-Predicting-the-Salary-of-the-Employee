## Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee
### AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

### Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook
### Algorithm
1.Import the libraries and read the data frame using pandas.

2.Calculate the null values present in the dataset and apply label encoder.

3.Determine test and training data set and apply decison tree regression in dataset.

4.Calculate Mean square error,data prediction and r2.

### Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Pravin Raj.A
RegisterNumber: 212222240079

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
### Output:
data.head()

![280511581-19fbcd18-73b3-4c29-92e9-be8d0ddebe46](https://github.com/Apravinraj/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707879/8ed23e3c-e317-43f5-ad5d-37da8771cafe)

data.info()

![280511603-063d157a-56c8-433b-ab29-aec5f79bd2b9](https://github.com/Apravinraj/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707879/3575a2dc-120a-42d1-ada9-b1e4cca6764c)

isnull() and sum()

![280511629-aff25c2b-ab6d-47a6-8182-b0798dcec4ec](https://github.com/Apravinraj/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707879/fdb8ee12-68a4-4cf0-9d98-141a37d14e33)

data.head() for salary

![280511654-baa81b57-f088-4b89-bc69-b20414dd5a53](https://github.com/Apravinraj/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707879/fa84ca02-83f7-4772-9350-73b984395230)


MSE value

![280511670-baeecf39-7832-4e2a-92e9-e86c782e2c5a](https://github.com/Apravinraj/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707879/e8755053-1279-40b3-a187-94a6c3385a58)


r2 value

![280511693-efeb2039-b686-4701-9b4d-3f2fd8ed5e0a](https://github.com/Apravinraj/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707879/81072c6b-f717-4c5c-8bfe-32ba7cb93547)


data prediction

![280511713-949fe7a3-b7c0-4981-a301-e5800ce2880c](https://github.com/Apravinraj/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707879/ade902e8-d60c-4bd5-9426-4de8a91bfc4d)

### Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
