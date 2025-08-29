# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Sidda Dhanush
RegisterNumber:  25005353
*/
```# Univariate Linear Regression using Least Squares Method
import numpy as np
import matplotlib.pyplot as plt

# Sample dataset (you can replace it with your own)
# x: independent variable, y: dependent variable
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

# Step 1: Calculate the mean of x and y
x_mean = np.mean(x)
y_mean = np.mean(y)

# Step 2: Calculate the slope (m) and intercept (c) using least squares
numerator = np.sum((x - x_mean) * (y - y_mean))
denominator = np.sum((x - x_mean) ** 2)
m = numerator / denominator
c = y_mean - m * x_mean

print(f"Slope (m): {m}")
print(f"Intercept (c): {c}")

# Step 3: Predict y values using the regression line
y_pred = m * x + c

# Step 4: Plot the results
plt.scatter(x, y, color='blue', label='Actual data')
plt.plot(x, y_pred, color='red', label='Regression line')
plt.xlabel('x')
plt.ylabel('y')
plt.title('Univariate Linear Regression - Least Squares')
plt.legend()
plt.grid(True)
plt.show()

## Output:
<img width="790" height="556" alt="Screenshot (2)" src="https://github.com/user-attachments/assets/ee508917-9487-458b-aea6-0aa65fc762f0" />

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
