# Correlation and Regression for Data Analysis
# Aim : 

To analyse given data using  coeffificient of correlation and regression line.
![image](https://user-images.githubusercontent.com/104613195/168224136-d6b64e64-7d3d-4775-9337-c8f96fe41f2d.png)


# Software required :  

Python

# Theory:

Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  

If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# Procedure :

![image](https://user-images.githubusercontent.com/104613195/168225866-ac8f6610-bdc3-4ac2-a24e-2b24ba08e189.png)

# Program
## Developed By: S.Sumyuktha Rani
## Register Number: 212220230042
```
import math
import numpy as np
import matplotlib.pyplot as plt
x=[25, 28, 35, 32, 31, 36, 29, 38, 34, 32]
y=[43, 46, 49, 41, 36, 32, 31, 30, 33, 39]
sx=0
sy=0
sxy=0
sx2=0
sy2=0
for i in range(0,10):
    sx=sx+x[i]
    sy=sy+y[i]
    sxy=sxy+x[i]*y[i]
    sx2=sx2+x[i]**2
    sy2=sy2+y[i]**2
    N=10
r=(N*sxy-sx*sy)/(math.sqrt(N*sx2-sx**2)*math.sqrt(N*sy2-sy**2))
print("The Correlation Coefficient is %0.3f"%r)

byx=(N*sxy-sx*sy)/(N*sx2-sx**2)
xmean=sx/N
ymean=sy/N
print("The regression line Y on X is ::: Y=%0.3f %0.3f (X- %0.3f)"% (ymean,byx,xmean))
plt.scatter(x,y)
def Reg(x):
    return ymean + byx*(x-xmean)
x=np.linspace(20,40,51)
y1=Reg(x)
plt.plot(x,y1,'r')
plt.xlabel('x-data')
plt.ylabel('y-data')
```
# Results and Output : 
![mt1](https://user-images.githubusercontent.com/75235032/170188208-b8cd6711-732d-4238-a5c9-d7cb02f24713.jpg)

Thus the analyzation of the given data using coeffificient of correlation and regression line has been successfully implemented.
