# lambda function

. user defined function it doesn't have a name

. lambda function are anomymous function

. lambda function always return the valueit is used as a input for high order function

. A funtion which takes another function as input is called as high order function

. lambda is a keyword

. the syntax is `lambda var/s:<statment/s using variable/s>`



```python
z[1,11]
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[11], line 1
    ----> 1 z[1,11]
    

    TypeError: list indices must be integers or slices, not tuple



```python
# example of a lambda function
z = (lambda x:x**2)(4)
z
```




    16




```python
(lambda x:x**11)(2)#finding the exponential form of x
```




    2048




```python
z = (lambda x:True if x%2==0 else False)(4)# even and odd number finding in single line
z
```




    True




```python
z
```




    True




```python
z = (lambda x,y:([ele for ele in range(x,y+1) if ele%2==0],[ele for ele in range(x,y+1) if ele%2!=0]))(1,30)
z
```




    ([2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30],
     [1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29])



# High order function : map,filter,reduce

 . High order function= A function which taj\kes another function as an input

# map

. we use map function to apply our function on each element of an iterator.

. The syntax is: `map(function,iterator)`

. output of mapfunction is a map object,we need to typecast it to a list or data type to see the output.


```python
z = [1 2 3]**2
```


      Cell In[25], line 1
        z = [1 2 3]**2
             ^
    SyntaxError: invalid syntax. Perhaps you forgot a comma?
    



```python
z = map(lambda x:x**2,[1,2,3])
z
```




    <map at 0x27013cc67d0>




```python
list(z)
```




    [1, 4, 9]




```python
z = map(ord, '!@#abyx')
z
```




    <map at 0x27013cc6290>




```python
list(z)
```




    [33, 64, 35, 97, 98, 121, 120]



map function does not shows any error.


```python
z = map(lambda x:x/0,[1,2,3])
z
```




    <map at 0x27013cc41c0>



but the list() shows an error


```python
list(z)
```


    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    Cell In[31], line 1
    ----> 1 list(z)
    

    Cell In[30], line 1, in <lambda>(x)
    ----> 1 z = map(lambda x:x/0,[1,2,3])
          2 z
    

    ZeroDivisionError: division by zero



```python
z = map(lambda x:x/2, [1,2,3],[4,5])
z
```




    <map at 0x27013cc9e70>




```python
list(z)# it show an error
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[36], line 1
    ----> 1 list(z)
    

    TypeError: <lambda>() takes 1 positional argument but 2 were given


# filter

. filter() function is a function used to filter the sequence of lists,tuples etc

. filter () is a built-in-function


```python
z = (filter(lambda x:True if x%2==0 else False,[1,2,3,4,5]))
z
```




    <filter at 0x27013b24640>




```python
list(z)
```




    [2, 4]




```python
z = (filter(lambda x:True if x=='a' else False, 'divya'))
z
```




    <filter at 0x27013b25540>




```python
list(z)
```




    ['a']




```python
z = (filter(lambda x:True if x in 'aeiouAEIOU' else False, 'divya'))# for finding the vowels in a string
z
```




    <filter at 0x27013b25090>




```python
list(z)
```




    ['i', 'a']




```python
h = filter(lambda x:True if x.isalnum() else False,'abc1234')
h
```




    <filter at 0x27013ccb7f0>




```python
list(h)
```




    ['a', 'b', 'c', '1', '2', '3', '4']




```python
z = filter(lambda x:True if x.isalnum() is False else False,'abc123$6')
z
```




    <filter at 0x27013b24370>




```python
list(z)
```




    ['$']




```python

```
