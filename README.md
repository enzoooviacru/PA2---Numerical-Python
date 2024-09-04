# PA2 - Numerical Python
PA2 submission of Lorenzo Viacrucis from 2ECE-D

NORMALIZATION PROBLEM

import numpy as np

#Creating an array with 5 rows and columns containing random elements
x = np.random.rand(5,5)

#Setting formulas to normalize th elements of array x
mean = x.mean()
std = x.std()
z = (x - mean)/std

#Saving the normalized array
np.save('X_normalized.npy', z)

#Printing non-normalized array
print("Non-normalized:")
print(x)

#Printing normalized array
print("Normalized:")
print(z)

DIVISIBLE BY 3 PROBLEM

import numpy as np

#Creating an array containing the first 100 positive integers
x = np.arange(1,101)

#Squaring the elements of the array
y = x**2

#Making the array into 10 rows and columns
z = y.reshape(10,10)

#Getting the elements divisible by 3 and putting it in its own array
divisible3 = y[y%3==0]

#Saving the array with elements divisible by 3
np.save('div_by_3.npy', divisible3)

#Printing the 10x10 array containing the square of the first 100 positive integers
print("The square of the first 100 positive integers are:")
print(z)

#Printing the elements of the 10x10 array that are divisible by 3
print("The integers that are divisibe by 3 are:")
print(divisible3)    
