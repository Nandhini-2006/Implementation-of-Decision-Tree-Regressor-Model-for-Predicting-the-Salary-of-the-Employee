# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values.

## Program:

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: NANDHINI N

RegisterNumber: 212224040212
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

import pandas as pd

data = pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

data["Position"] = le.fit_transform(data["Position"])

data.head()

x = data[["Position", "Level"]]

y = data["Salary"]

from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)

from sklearn.tree import DecisionTreeRegressor

dt = DecisionTreeRegressor()

dt.fit(x_train, y_train)

y_pred = df.predict(x_test)

from sklearn import metrics

mse = metrics.mean_squared_error(y_test, y_pred)

mse

r2 = metrics.r2_score(y_test, y_pred)

r2

dt.predict([[5,6]])

## Output:

![Screenshot 2025-05-19 155059](https://github.com/user-attachments/assets/1ed6f9cd-2c49-4e52-bdf9-de994c24a373)

![Screenshot 2025-05-19 155105](https://github.com/user-attachments/assets/6a3d3513-1bbb-4826-8ebb-6b7613ada5d4)

![Screenshot 2025-05-19 155111](https://github.com/user-attachments/assets/7972a7ce-b8fe-445c-a0af-719e44d17512)

![Screenshot 2025-05-19 155119](https://github.com/user-attachments/assets/65aca1df-a6a8-49dd-baf5-72a23b721c3e)

![Screenshot 2025-05-19 155125](https://github.com/user-attachments/assets/f68cd880-feb5-4c84-96be-ae3ddc090c43)

![Screenshot 2025-05-19 155131](https://github.com/user-attachments/assets/f5e6ff81-9520-49bd-863d-fd9220c1e98c)

![Screenshot 2025-05-19 155136](https://github.com/user-attachments/assets/497cf426-5535-4a30-b747-4a42fd526ac7)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
