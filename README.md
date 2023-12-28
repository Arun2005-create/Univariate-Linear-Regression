# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
# Program for Univariate linear regression using the least squares method.
# Developed by: Arun Kumar B
# Register Number: 23004514
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
mnx=np.mean(X)
mny=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-mnx)*(Y[i]-mny)
    den+=(X[i]-mnx)**2
m=num/den
c=mny-m*mnx
print(m,c)
p=m*X+c
print(p)
plt.scatter(X,Y,color='blue')
plt.plot(X,p,color='red')
plt.show()





```
## Output
![Screenshot 2023-12-28 120932](https://github.com/Arun2005-create/Univariate-Linear-Regression/assets/138849356/8adda75c-d38c-49dd-a44e-9e9a672c2a9a)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
