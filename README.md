# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import Required Libraries and Load the Dataset  
2. Preprocess the Data (Check Missing Values and Encode Categorical Features)  
3. Select Features and Target Variable  
4. Split the Data and Train the Decision Tree Regressor  
5. Predict and Evaluate the Model using Mean Squared Error and R² Score  


## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: GAYATHRI.C
RegisterNumber:  25009125

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
from sklearn import metrics
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2) 
from sklearn.tree import DecisionTreeRegressor 
dt=DecisionTreeRegressor() 
dt.fit(x_train,y_train) 
y_pred=dt.predict(x_test) 
print(y_pred )

mse=metrics.mean_squared_error(y_test, y_pred)
print(mse)
r2= metrics.r2_score(y_test,y_pred)
print(r2)
dt.predict([[5,6]])
```

## Output:
## Data head:
![WhatsApp Image 2025-10-06 at 14 41 45_5c55bb3e](https://github.com/user-attachments/assets/59f5e510-f5b2-41a2-b302-16f8bb5f96ac)
## Data info:
![WhatsApp Image 2025-10-06 at 14 40 10_477f5214](https://github.com/user-attachments/assets/7727ceab-5a05-446b-bca0-a5cb44e663e3)
## Data head for salary:
![WhatsApp Image 2025-10-06 at 14 40 37_1c825bdb](https://github.com/user-attachments/assets/cf179469-add9-4bb8-9d4c-6f8b96baa8d4)
## isnull().sum()
![WhatsApp Image 2025-10-06 at 14 41 04_9cf40cc6](https://github.com/user-attachments/assets/4ac9b2d6-8e99-4966-9b6d-74f4d0b4f420)
## Mean square error and r2 value
![WhatsApp Image 2025-10-06 at 14 38 04_13d3b4e8](https://github.com/user-attachments/assets/33f375bb-75d4-42fc-b1a8-10b0a39c7b13)
## Prediction
![WhatsApp Image 2025-10-06 at 14 38 24_ff2fc121](https://github.com/user-attachments/assets/c0cf48da-7ae6-47f9-a3bf-6aa71d3cf31f)








## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
