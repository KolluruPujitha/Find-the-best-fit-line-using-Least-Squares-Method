# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

STEP 1.Start

STEP 2. Get the independent variable X and dependent variable Y.

STEP 3. Calculate the mean of the X -values and the mean of the Y -values.

STEP 4. Find the slope m of the line of best fit using the formula. 
        <img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
        
STEP 5. Compute the y -intercept of the line by using the formula:
        <img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
        
STEP 6. Use the slope m and the y -intercept to form the equation of the line.

STEP 7. Obtain the straight line equation Y=mX+b and plot the scatterplot.

STEP 8.End

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: KOLLURU PUJITHA
RegisterNumber: 212223240074
*/
import numpy as np
import matplotlib.pyplot as plt

#Preprocessing input data

x=np.array(eval(input()))
y=np.array(eval(input()))

#Mean

x_mean=np.mean(x)
y_mean=np.mean(y)
num=0 #Slope
denom=0 #Slope

#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2

#calculate slope
m=num/denom

#calculate intercept
b=y_mean-m*x_mean
print(m,b)
#Line equation
y_predicted=m*x+b
print(y_predicted)

#to plot graph
plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()
```

## Output:
## Slope and output:
![Screenshot 2024-08-23 105720](https://github.com/user-attachments/assets/db537060-caff-4fc9-ba1e-79198ea8b7e5)
## y predicted:
![Screenshot 2024-08-23 105720](https://github.com/user-attachments/assets/e7070014-7643-4a60-b3df-b9f0835bc59e)
## Graph:
![image](https://github.com/user-attachments/assets/020decfa-acd6-44dc-826b-c212cf7214c4)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
