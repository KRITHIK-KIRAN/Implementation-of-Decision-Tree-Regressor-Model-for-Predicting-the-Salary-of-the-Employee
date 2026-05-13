# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the salary dataset using Pandas and separate the input features (X) and target variable (y).
2.Convert categorical variables into numerical form using one-hot encoding and split the dataset into training and testing sets.
3.Train a DecisionTreeRegressor model on the training data using the Scikit-learn library.
4.Visualize the trained decision tree using Matplotlib and plot_tree() to display the regression model structure. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Krithik kiran .S
RegisterNumber:212225230145
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor, plot_tree
data = pd.read_csv("Salary (1).csv")
X = data.drop("Salary", axis=1)
y = data["Salary"]
X = pd.get_dummies(X, drop_first=True)
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42)
model = DecisionTreeRegressor(random_state=42)
model.fit(X_train, y_train)
plt.figure(figsize=(25,12))
plot_tree(
    model,
    feature_names=X.columns,
    filled=True
)

plt.title("Decision Tree Regressor")
plt.show()

*/
```

## Output:
<img width="1389" height="689" alt="image" src="https://github.com/user-attachments/assets/804cff5c-01a6-40b2-8022-120d1fa4e9a5" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
