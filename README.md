# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the dataset and separate input and output variables.

2.Split the data into training and testing sets.

3.Train the linear regression model using the training data.

4.Predict the output for the test data and evaluate the results. 

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: BUSHRA FATHIMA I
RegisterNumber: 212225040051
*/

import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression


X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

model = LinearRegression()

model.fit(X, Y)

m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)

x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])

Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()

```

## Output:
<img width="880" height="673" alt="Screenshot 2026-04-21 112015" src="https://github.com/user-attachments/assets/284ce01b-0283-433f-950e-03f29043f125" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
