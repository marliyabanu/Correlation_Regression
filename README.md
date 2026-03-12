# Correlation and regression for data analysis
# Aim : 

To analyse given data using coeffificient of correlation and regression line
![image](https://user-images.githubusercontent.com/104613195/168224136-d6b64e64-7d3d-4775-9337-c8f96fe41f2d.png)


# Software required :  

Python

# Theory:

Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  

If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# Procedure :

![image](https://user-images.githubusercontent.com/104613195/168225866-ac8f6610-bdc3-4ac2-a24e-2b24ba08e189.png)

# Program :
Developed by: Marliya Banu B

Reg no: 212225040229
~~~
import numpy as np
import math
import matplotlib.pyplot as plt
x=[ int(i) for i in input().split()]
y=[ int(i) for i in input().split()]
N=len(x)
Sx=0
Sy=0
Sxy=0
Sx2=0
Sy2=0
for i in range(0,N):
    Sx=Sx+x[i]
    Sy=Sy+y[i]
    Sxy=Sxy+x[i]*y[i]
    Sx2=Sx2+x[i]**2
    Sy2=Sy2+y[i]**2
r=(N*Sxy-Sx*Sy)/(math.sqrt(N*Sx2-Sx**2)*math.sqrt(N*Sy2-Sy**2))
print("The Correlation coefficient is %0.3f"%r)
byx=(N*Sxy-Sx*Sy)/(N*Sx2-Sx**2)
xmean=Sx/N
ymean=Sy/N
print("The Regression line Y on X is ::: y = %0.3f + %0.3f (x-%0.3f)"%(ymean,byx,xmean))
plt.scatter(x,y)
def Reg(x):
  return ymean + byx*(x-xmean)
x1=np.linspace(20,80,51)
y1=Reg(x1)
plt.plot(x1,y1,'r')
plt.xlabel('x-data')
plt.ylabel('y-data')
plt.legend(['Regression Line','Data points'])
plt.show()

~~~

# Output 
https://private-user-images.githubusercontent.com/182350057/396917735-59035544-2459-4372-b6ad-6ef026556627.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NzMzMTA5MDEsIm5iZiI6MTc3MzMxMDYwMSwicGF0aCI6Ii8xODIzNTAwNTcvMzk2OTE3NzM1LTU5MDM1NTQ0LTI0NTktNDM3Mi1iNmFkLTZlZjAyNjU1NjYyNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYwMzEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MDMxMlQxMDE2NDFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zMzIxZDk2NTI2Yzc0ODk5YTVlNTM5NmQ3ZTYwZmUyODU0YmFlMzFiY2JkNTdhNzEwNzRiNDYzNTMwMGE2ZmNmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.PwwaeH5KY5---d3A5Z1Unf2QvmVHZ1mDU6PfvSKX4bY

# Result
The Correlation and Regression for data analysis of objects from feeder using probability distributed are calculated.
