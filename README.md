# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display.

## Program:
```python
##Program to find the solution of a matrix using Gaussian Elimination.
##Developed by: ANDREW VARGHESE VS
##RegisterNumber: 212222103001
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in  range(n):
    print('X%d = %0.2f'%(i,x[i]),end = ' ') 
```

## Output:
<img width="995" alt="Screenshot 2023-11-17 at 5 08 09 PM" src="https://github.com/Andrewvarghese653/Gaussian/assets/145822115/c05da722-0460-48d7-9296-167bf7204bf7">
<img width="885" alt="Screenshot 2023-11-17 at 5 13 51 PM" src="https://github.com/Andrewvarghese653/Gaussian/assets/145822115/9d744deb-4f5a-4eca-ae3f-f90402ccc68f">




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

