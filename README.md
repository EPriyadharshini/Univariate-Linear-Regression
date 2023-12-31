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

#program to find univariate linear regression
#Developed By: E.PRIYADHARSHINI
#Register no : 23012593

import numpy as np
import matplotlib.pyplot as plt
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y,color='cyan')
plt.show()
xmean=np.mean(x)
ymean=np.mean(y)
num=0
den=0
for i in range(len(x)):
  num+=(x[i]-xmean)*(y[i]-ymean)
  den+=(x[i]-xmean)**2
m=num/den
b=ymean-m*xmean
print(m,b)
ypred=m*x+b
print(ypred)
plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()

```
## Output

<img width="334" alt="image" src="https://github.com/EPriyadharshini/Univariate-Linear-Regression/assets/144870831/5bd4c168-9528-44f1-8585-7cf5cd3bae02">

![Screenshot 2023-12-26 151813](https://github.com/23004205/Univariate-Linear-Regression/assets/138971114/b9392a7e-a69d-4929-bd7a-365272daa922)
![Screenshot 2023-12-26 151828](https://github.com/23004205/Univariate-Linear-Regression/assets/138971114/dac4465f-beaf-4135-a6ce-3cd4972dc6c6)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
