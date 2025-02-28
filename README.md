
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
Developed by: Keerthika.S
RegisterNumber: 212223040093 
*/
```
```
import numpy as np
import matplotlib.pyplot as plt

x = np.array(eval(input("Enter x values (e.g., [1, 2, 3]): ")))
y = np.array(eval(input("Enter y values (e.g., [2, 4, 5]): ")))

x_mean = np.mean(x)
y_mean = np.mean(y)

num = np.sum((x - x_mean) * (y - y_mean))
denom = np.sum((x - x_mean)**2)

m = num / denom
b = y_mean - m * x_mean

print(f"Slope (m): {m}")
print(f"Intercept (b): {b}")

y_predicted = m * x + b
print(f"Predicted y values: {y_predicted}")

plt.scatter(x, y, label="Data points")
plt.plot(x, y_predicted, color='red', label="Fitted line")
plt.legend()
plt.show()
```

## Output:
![best fit line](sam.png)
```
Enter x values (e.g., [1, 2, 3]): 8,2,11,6,5,4,12,9,6,1
Enter y values (e.g., [2, 4, 5]): 3,10,3,6,8,12,1,4,9,14
Slope (m): -1.106418918918919
Intercept (b): 14.081081081081082
Predicted y values: [ 5.22972973 11.86824324  1.91047297  7.44256757  8.54898649  9.65540541
  0.80405405  4.12331081  7.44256757 12.97466216]

```
![416958626-2e72078a-0660-414c-9a51-659ca1116875](https://github.com/user-attachments/assets/e6475058-65a7-4493-bb9d-c6693f3f7b47)


## Result:

Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
