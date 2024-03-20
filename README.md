# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1 import numberical python
2 import sys
3 give the input
4 type the required functions

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Sana Fathima H
RegisterNumber: 212223240145
'''
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
X=np.zeros(n)
for i in range (n):
    for j in range(n+1):
        matrix [i][j]=int(input())
for i in range (n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
X[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i]=matrix[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-matrix[i][j]*X[j]
    X[i]=X[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,X[i]),end=" ")
```

## Output:
![Screenshot 2024-03-20 033539](https://github.com/Sanafathima95773/Gaussian/assets/147084627/7e424bd0-6400-4c94-8f04-f9f4a0888d92)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

