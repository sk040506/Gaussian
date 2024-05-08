# Gaussian Elimination


## AIM:

To write a program to find the solution of a matrix using Gaussian Elimination.


## Equipments Required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner



## Algorithm

1. Import numpy library using import statement.
2. Import the sys module to use the built-in functions.
3. Get input from the user for number of rows and add it by 1 for number of columns.
4. Using np.zeros() set the matrix as null matrix
5. Using for loop get input from the user for each element in the matrix.
6. Using for loop we can perform the elementary row operations and find the final matrix.
7. Print the values by solving the matrix using for loop with 2 point precision.
8. End the program.


## Program:

```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: sk balaji
Register Number:  2305003001


import numpy as py
import sys

n=int(input())

a=np.zeros((n,n+1))

x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())

for i in range(n):
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k] - ratio *a[i][k]

x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]

for i in range(n):
    print('x%d = %0.2f' %(i,x[i]),end= ' ')

```

## Output:

![image](https://github.com/sk040506/Gaussian/assets/155505137/7c56d0cc-0c05-4c3c-9c0a-7b8b91f20b61)
![image](https://github.com/sk040506/Gaussian/assets/155505137/03dfa649-0642-4df9-ab39-6d59249d3f67)




## Result:

Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

