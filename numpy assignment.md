1. Given are 2 similar dimensional numpy arrays, how to get a numpy array output
in which every element is an element-wise sum of the 2 numpy arrays?

```python
import numpy as np
a=np.array([1,2,3,4])
b=np.array([6,7,5,4])
print(a+b)
```

    [7 9 8 8]
    
2. Given a numpy array (matrix), how to get a numpy array output which is equal to
the original matrix multiplied by a scalar?

```python
m=np.array([[1,2,3],[4,5,6],[8,9,7]])
4*m
```




    array([[ 4,  8, 12],
           [16, 20, 24],
           [32, 36, 28]])


3. Create an identity matrix of dimension 4-by-4.

```python
np.eye(4)
```




    array([[1., 0., 0., 0.],
           [0., 1., 0., 0.],
           [0., 0., 1., 0.],
           [0., 0., 0., 1.]])


4. Convert a 1-D array to a 3-D array

```python
np.array([1,2,3,4,5,6,7,8]).reshape(2,2,2)
```




    array([[[1, 2],
            [3, 4]],
    
           [[5, 6],
            [7, 8]]])


5. Convert a binary numpy array (containing only 0s and 1s) to a boolean numpy
array

```python
a=np.array([[1,0,1,0],[0,1,1,0]],dtype='bool')
a
```




    array([[ True, False,  True, False],
           [False,  True,  True, False]])


6. Convert all the elements of a numpy array from float to integer datatype

```python
a=np.array([[1,0,5,0],[79,1,1,0]],dtype='float')
print(a.dtype)
a=a.astype('int32')
print(a.dtype)
```

    float64
    int32
    
7. Stack 2 numpy arrays horizontally i.e., 2 arrays having the same 1st dimension
(number of rows in 2D arrays)


```python
a=np.array([1,2,3,4])
b=np.array([5,6,7,8])
np.array((a,b))
```




    array([[1, 2, 3, 4],
           [5, 6, 7, 8]])


8. Output a sequence of equally gapped 5 numbers in the range 0 to 100 (both
inclusive)

```python
np.arange(0,101,5)
```




    array([  0,   5,  10,  15,  20,  25,  30,  35,  40,  45,  50,  55,  60,
            65,  70,  75,  80,  85,  90,  95, 100])


9. Output a matrix (numpy array) of dimension 2-by-3 with each and every value
equal to 5


```python
a=5*np.ones(3,dtype='int32')
np.array((a,a))
```




    array([[5, 5, 5],
           [5, 5, 5]])


10.Given 2 numpy arrays as matrices, output the result of multiplying the 2 matrices
(as a numpy array)

```python
a=np.array([1,2,3,4,5,6,7,8,9]).reshape(3,3)
print(a)
a*a
```

    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    




    array([[ 1,  4,  9],
           [16, 25, 36],
           [49, 64, 81]])


11. Output the array element indexes such that the array elements appear in the
ascending order

```python
a=np.array([4,6,1,8,3,9],dtype='int32')
print(a)
a.sort()
a
```

    [4 6 1 8 3 9]
    




    array([1, 3, 4, 6, 8, 9])


12.Multiply a 5x3 matrix by a 3x2 matrix (real matrix product)

```python
a=np.array([1,2,3,4,5,6,7,8,9,10,3,4,5,8,5],dtype='int32').reshape(5,3)
b=np.array([1,2,3,4,5,6],dtype='int32').reshape(3,2)
print(a)
print()
print(b)
np.dot(a,b)
```

    [[ 1  2  3]
     [ 4  5  6]
     [ 7  8  9]
     [10  3  4]
     [ 5  8  5]]
    
    [[1 2]
     [3 4]
     [5 6]]
    




    array([[ 22,  28],
           [ 49,  64],
           [ 76, 100],
           [ 39,  56],
           [ 54,  72]])




```python
a.index(5)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-5-d81d2b00d317> in <module>
    ----> 1 a.index(5)
    

    AttributeError: 'numpy.ndarray' object has no attribute 'index'



```python
a=np.random.randint(10,size=(3,5,6,4,3))
```


```python
a
```




    array([[[[[5, 7, 8],
              [3, 3, 1],
              [2, 3, 0],
              [3, 0, 6]],
    
             [[2, 2, 9],
              [2, 1, 2],
              [1, 3, 0],
              [7, 9, 5]],
    
             [[2, 9, 8],
              [0, 7, 6],
              [7, 4, 1],
              [5, 6, 8]],
    
             [[8, 8, 8],
              [9, 8, 1],
              [2, 8, 9],
              [2, 4, 4]],
    
             [[4, 2, 2],
              [3, 9, 9],
              [9, 8, 8],
              [9, 8, 7]],
    
             [[9, 4, 7],
              [3, 6, 4],
              [1, 9, 7],
              [3, 9, 7]]],
    
    
            [[[4, 4, 2],
              [0, 1, 7],
              [8, 3, 3],
              [7, 9, 1]],
    
             [[6, 8, 7],
              [9, 8, 8],
              [3, 9, 5],
              [2, 9, 8]],
    
             [[9, 5, 4],
              [3, 2, 8],
              [4, 5, 9],
              [2, 2, 9]],
    
             [[5, 3, 3],
              [2, 4, 7],
              [8, 0, 6],
              [2, 9, 3]],
    
             [[1, 1, 8],
              [2, 1, 8],
              [6, 3, 0],
              [3, 8, 5]],
    
             [[3, 5, 7],
              [3, 7, 8],
              [1, 3, 0],
              [0, 7, 1]]],
    
    
            [[[2, 2, 5],
              [6, 8, 1],
              [9, 7, 3],
              [4, 3, 2]],
    
             [[8, 9, 3],
              [2, 9, 5],
              [3, 5, 1],
              [9, 7, 3]],
    
             [[7, 6, 5],
              [2, 8, 3],
              [3, 3, 7],
              [4, 9, 6]],
    
             [[2, 6, 8],
              [7, 5, 8],
              [8, 0, 8],
              [4, 9, 3]],
    
             [[3, 8, 4],
              [4, 0, 5],
              [3, 8, 3],
              [0, 4, 0]],
    
             [[9, 2, 6],
              [9, 0, 6],
              [0, 9, 6],
              [3, 4, 0]]],
    
    
            [[[3, 7, 9],
              [4, 6, 7],
              [2, 8, 8],
              [6, 1, 4]],
    
             [[8, 5, 0],
              [2, 1, 3],
              [5, 0, 7],
              [3, 6, 1]],
    
             [[7, 9, 0],
              [6, 5, 6],
              [6, 3, 1],
              [3, 3, 0]],
    
             [[8, 0, 7],
              [2, 6, 5],
              [7, 5, 0],
              [0, 5, 7]],
    
             [[0, 4, 3],
              [2, 0, 8],
              [8, 4, 9],
              [1, 1, 2]],
    
             [[5, 3, 4],
              [9, 7, 8],
              [7, 8, 9],
              [7, 4, 6]]],
    
    
            [[[8, 6, 9],
              [4, 5, 7],
              [0, 1, 5],
              [9, 0, 3]],
    
             [[0, 6, 2],
              [1, 5, 2],
              [3, 2, 8],
              [4, 8, 6]],
    
             [[6, 5, 8],
              [7, 1, 1],
              [6, 6, 5],
              [7, 2, 8]],
    
             [[0, 6, 9],
              [3, 7, 1],
              [4, 4, 2],
              [5, 5, 3]],
    
             [[4, 0, 0],
              [0, 5, 5],
              [3, 7, 0],
              [4, 7, 5]],
    
             [[8, 3, 0],
              [0, 5, 4],
              [1, 5, 0],
              [5, 2, 4]]]],
    
    
    
           [[[[4, 0, 5],
              [7, 6, 2],
              [6, 4, 9],
              [6, 8, 5]],
    
             [[6, 4, 6],
              [4, 4, 7],
              [2, 4, 6],
              [5, 4, 7]],
    
             [[5, 2, 7],
              [8, 9, 2],
              [0, 6, 4],
              [0, 4, 3]],
    
             [[5, 0, 6],
              [5, 8, 0],
              [9, 5, 7],
              [7, 3, 9]],
    
             [[0, 9, 8],
              [5, 7, 0],
              [8, 9, 4],
              [6, 0, 3]],
    
             [[7, 8, 0],
              [6, 7, 5],
              [4, 1, 2],
              [6, 2, 1]]],
    
    
            [[[8, 2, 1],
              [4, 9, 7],
              [9, 8, 5],
              [5, 8, 5]],
    
             [[8, 4, 9],
              [9, 8, 2],
              [2, 2, 2],
              [7, 5, 6]],
    
             [[7, 7, 7],
              [3, 2, 6],
              [6, 5, 8],
              [7, 7, 3]],
    
             [[1, 3, 5],
              [7, 1, 3],
              [2, 6, 2],
              [2, 6, 1]],
    
             [[7, 1, 4],
              [8, 5, 7],
              [1, 3, 6],
              [1, 5, 3]],
    
             [[0, 6, 6],
              [0, 5, 2],
              [8, 9, 7],
              [0, 4, 4]]],
    
    
            [[[2, 1, 5],
              [6, 6, 2],
              [0, 9, 3],
              [5, 5, 5]],
    
             [[8, 7, 6],
              [9, 6, 6],
              [9, 2, 0],
              [9, 0, 8]],
    
             [[5, 2, 9],
              [8, 8, 1],
              [0, 0, 9],
              [0, 8, 3]],
    
             [[7, 1, 6],
              [1, 8, 0],
              [4, 3, 6],
              [4, 9, 4]],
    
             [[6, 7, 1],
              [7, 3, 6],
              [8, 1, 4],
              [9, 0, 2]],
    
             [[3, 8, 0],
              [5, 1, 4],
              [6, 5, 1],
              [9, 3, 2]]],
    
    
            [[[6, 2, 0],
              [3, 8, 7],
              [9, 3, 6],
              [3, 6, 1]],
    
             [[1, 3, 3],
              [3, 9, 1],
              [7, 0, 1],
              [5, 0, 4]],
    
             [[5, 6, 4],
              [1, 2, 9],
              [6, 5, 0],
              [2, 2, 3]],
    
             [[7, 1, 8],
              [6, 8, 3],
              [0, 1, 2],
              [0, 9, 6]],
    
             [[3, 6, 9],
              [5, 8, 6],
              [5, 4, 3],
              [1, 9, 2]],
    
             [[4, 2, 0],
              [8, 1, 7],
              [5, 8, 9],
              [2, 3, 2]]],
    
    
            [[[4, 4, 2],
              [7, 4, 0],
              [5, 0, 2],
              [9, 3, 7]],
    
             [[0, 2, 4],
              [0, 4, 7],
              [5, 1, 9],
              [8, 3, 8]],
    
             [[6, 9, 1],
              [2, 1, 7],
              [2, 2, 2],
              [9, 3, 6]],
    
             [[5, 5, 4],
              [3, 3, 1],
              [2, 5, 0],
              [3, 9, 6]],
    
             [[8, 3, 4],
              [8, 5, 3],
              [3, 0, 8],
              [5, 4, 9]],
    
             [[2, 0, 6],
              [2, 3, 4],
              [9, 3, 0],
              [4, 8, 5]]]],
    
    
    
           [[[[0, 9, 3],
              [7, 5, 6],
              [8, 0, 7],
              [4, 5, 8]],
    
             [[2, 8, 1],
              [2, 4, 3],
              [8, 7, 9],
              [7, 4, 9]],
    
             [[6, 3, 1],
              [0, 8, 1],
              [6, 9, 6],
              [7, 3, 1]],
    
             [[1, 7, 1],
              [6, 5, 2],
              [2, 2, 2],
              [8, 6, 2]],
    
             [[6, 3, 0],
              [0, 5, 4],
              [4, 7, 1],
              [2, 5, 3]],
    
             [[3, 8, 4],
              [5, 2, 1],
              [5, 2, 0],
              [8, 7, 6]]],
    
    
            [[[3, 4, 9],
              [0, 7, 2],
              [5, 7, 3],
              [3, 5, 0]],
    
             [[7, 8, 1],
              [5, 5, 2],
              [6, 9, 2],
              [0, 1, 4]],
    
             [[2, 4, 1],
              [2, 5, 4],
              [8, 9, 9],
              [4, 8, 3]],
    
             [[2, 8, 5],
              [8, 4, 3],
              [2, 7, 0],
              [4, 5, 9]],
    
             [[3, 4, 0],
              [7, 4, 4],
              [7, 2, 5],
              [3, 6, 0]],
    
             [[0, 3, 4],
              [4, 7, 0],
              [7, 5, 9],
              [9, 5, 0]]],
    
    
            [[[5, 7, 6],
              [9, 1, 4],
              [3, 0, 8],
              [2, 3, 7]],
    
             [[8, 3, 8],
              [6, 4, 8],
              [9, 7, 5],
              [0, 0, 3]],
    
             [[0, 6, 8],
              [9, 6, 2],
              [8, 3, 1],
              [3, 4, 0]],
    
             [[1, 5, 7],
              [3, 9, 8],
              [4, 5, 0],
              [0, 4, 0]],
    
             [[6, 9, 3],
              [0, 7, 7],
              [5, 9, 9],
              [7, 4, 9]],
    
             [[0, 7, 8],
              [5, 8, 5],
              [1, 1, 0],
              [5, 7, 5]]],
    
    
            [[[5, 3, 9],
              [3, 9, 6],
              [4, 6, 1],
              [8, 1, 1]],
    
             [[3, 6, 6],
              [8, 7, 8],
              [4, 7, 3],
              [5, 2, 1]],
    
             [[2, 9, 9],
              [3, 6, 3],
              [5, 4, 5],
              [1, 1, 5]],
    
             [[9, 7, 6],
              [4, 3, 3],
              [8, 7, 1],
              [9, 9, 2]],
    
             [[9, 9, 4],
              [8, 0, 8],
              [1, 9, 5],
              [3, 1, 1]],
    
             [[4, 0, 0],
              [2, 2, 0],
              [4, 4, 4],
              [6, 4, 0]]],
    
    
            [[[8, 2, 3],
              [1, 5, 2],
              [3, 3, 6],
              [4, 7, 0]],
    
             [[3, 4, 3],
              [2, 9, 5],
              [3, 8, 2],
              [3, 1, 7]],
    
             [[5, 7, 4],
              [6, 5, 1],
              [3, 6, 4],
              [3, 0, 4]],
    
             [[0, 4, 9],
              [1, 6, 0],
              [5, 9, 5],
              [5, 2, 6]],
    
             [[3, 5, 5],
              [5, 3, 3],
              [5, 0, 2],
              [6, 4, 6]],
    
             [[2, 5, 3],
              [9, 6, 3],
              [9, 3, 7],
              [8, 5, 8]]]]])




```python
a[-1,-1,-1,-2:,-1]
```




    array([7, 8])



# Assignment 2

1. Write a NumPy program to convert a list of numeric values into a one-dimensional NumPy array. 


```python
import numpy as np
a=[1,2,3,4]
np.array(a)
```




    array([1, 2, 3, 4])



2. Write a NumPy program to create a 4x4 matrix with values ranging from 7 to 15. 


```python
np.random.randint(low=7,high=16,size=(3,2,2,3))
```




    array([[[[ 9, 15,  9],
             [11, 11, 14]],
    
            [[15, 14, 11],
             [12, 11,  7]]],
    
    
           [[[ 7, 15,  8],
             [14, 13, 12]],
    
            [[10,  9, 11],
             [10, 15, 11]]],
    
    
           [[[10, 15, 11],
             [14,  8, 12]],
    
            [[ 9,  9, 14],
             [13, 12, 11]]]])



3. Write a NumPy program to create a null vector of size 10 and update the sixth value to 11.


```python
a=np.zeros(10,dtype='int32')
a[5]=11
a
```




    array([ 0,  0,  0,  0,  0, 11,  0,  0,  0,  0])



4. Write a NumPy program to reverse an array (first element becomes last).


```python
a=[1,2,3,4,5,6]
a=np.array(a)
b=[]
for i in range(len(a)-1,-1,-1):
    b.append(a[i])
np.array(b)
```




    array([6, 5, 4, 3, 2, 1])



5. Write a NumPy program to create a 2d array with 1 on the border and 0 inside


```python
a=np.zeros(9,dtype='int32')
a=a.reshape(3,3)
np.pad(a,1,constant_values=1)
```




    array([[1, 1, 1, 1, 1],
           [1, 0, 0, 0, 1],
           [1, 0, 0, 0, 1],
           [1, 0, 0, 0, 1],
           [1, 1, 1, 1, 1]])



6. Write a NumPy program to create a 8x8 matrix and fill it with a checkerboard pattern.


```python
np.array((([0,1]*4)+[1,0]*4)*4).reshape(8,8)
```




    array([[0, 1, 0, 1, 0, 1, 0, 1],
           [1, 0, 1, 0, 1, 0, 1, 0],
           [0, 1, 0, 1, 0, 1, 0, 1],
           [1, 0, 1, 0, 1, 0, 1, 0],
           [0, 1, 0, 1, 0, 1, 0, 1],
           [1, 0, 1, 0, 1, 0, 1, 0],
           [0, 1, 0, 1, 0, 1, 0, 1],
           [1, 0, 1, 0, 1, 0, 1, 0]])



7. Write a NumPy program to append values to the end of an array.


```python
a=8
b=np.array([1,2,3,4,5])
np.append(b,a)
```




    array([1, 2, 3, 4, 5, 8])



8. Write a NumPy program to convert the values of Centigrade degrees into Fahrenheit degrees and vice versa. Values are stored into a NumPy array.


```python
a=np.arange(0,16).reshape(4,4)
a,a+273
```




    (array([[ 0,  1,  2,  3],
            [ 4,  5,  6,  7],
            [ 8,  9, 10, 11],
            [12, 13, 14, 15]]),
     array([[273, 274, 275, 276],
            [277, 278, 279, 280],
            [281, 282, 283, 284],
            [285, 286, 287, 288]]))



9. Write a NumPy program to find the number of elements of an array, length of one array element in bytes and total bytes consumed by the elements.


```python
a.size,a.itemsize,a.nbytes
```




    (16, 4, 64)



10. Write a NumPy program to test whether each element of a 1-D array is also present in a second array


```python
 for i in b:
    if i in a:
        print('yes')
    else:
        print('no')
```

    yes
    yes
    yes
    yes
    yes
    

11. Write a NumPy program to create an array of ones and an array of zeros.


```python
np.ones(10),np.zeros(5)
```




    (array([1., 1., 1., 1., 1., 1., 1., 1., 1., 1.]), array([0., 0., 0., 0., 0.]))



12. Write a NumPy program to create a new shape to an array without changing its data


```python
print(a)
a=a.reshape(2,2,2,2)
print(a)
```

    [[ 0  1  2  3]
     [ 4  5  6  7]
     [ 8  9 10 11]
     [12 13 14 15]]
    [[[[ 0  1]
       [ 2  3]]
    
      [[ 4  5]
       [ 6  7]]]
    
    
     [[[ 8  9]
       [10 11]]
    
      [[12 13]
       [14 15]]]]
    

13. Write a NumPy program to change the data type of an array.


```python
print(a.dtype)
a=a.astype('float64')
print(a.dtype)
```

    int32
    float64
    

14. Write a NumPy program to create a new array of 3*5, filled with 2.


```python
b=np.ones(15).reshape(3,5)
print(b*1)
```

    [[1. 1. 1. 1. 1.]
     [1. 1. 1. 1. 1.]
     [1. 1. 1. 1. 1.]]
    

15. Write a NumPy program to create a 3-D array with ones on a diagonal and zeros elsewhere


```python
c=np.eye(4)
c=np.array((c,c,c))
c
```




    array([[[1., 0., 0., 0.],
            [0., 1., 0., 0.],
            [0., 0., 1., 0.],
            [0., 0., 0., 1.]],
    
           [[1., 0., 0., 0.],
            [0., 1., 0., 0.],
            [0., 0., 1., 0.],
            [0., 0., 0., 1.]],
    
           [[1., 0., 0., 0.],
            [0., 1., 0., 0.],
            [0., 0., 1., 0.],
            [0., 0., 0., 1.]]])




```python

```
