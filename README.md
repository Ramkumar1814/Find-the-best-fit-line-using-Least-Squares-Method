# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
step 1: Start 
step 2: Get the independent variable X and dependent variable Y.
step 3: Calculate the mean of the X -values and the mean of the Y -values.
step 4: Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
step 5: Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
step 6: Use the slope m and the y -intercept to form the equation of the line.
step 7: Obtain the straight line equation Y=mX+b and plot the scatterplot.
step 8:End

## Program:

import numpy as np
import matplotlib.pyplot as plt 
X = np.array(eval(input()))
Y = np.array(eval(input()))
 
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
    
m=num/denom

b=Y_mean-m*X_mean

print(m,b)
y_predicted=m*X+b
print(y_predicted)

plt.scatter(X,Y)
plt.plot(X,y_predicted,color='blue')
plt.show

## Output:
## slope And Intercept
-4.492455418381343 35.7517146776406
## Y Intercept
![Screenshot 2024-08-23 111138](https://github.com/user-attachments/assets/b22cffb8-e60a-4ff4-965b-8ba348f93891)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
