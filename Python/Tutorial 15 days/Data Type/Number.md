There are three numeric types in Python:

- `int`
- `float`
- `complex`

#### Example 

```python
x = 1    # int  
y = 2.8  # float  
z = 1j   # complex
c = 3 + 1j   # complex
```

#### Check Data Type 

```python
print(type(x))  
print(type(y))  
print(type(z))
print(type(c))
```

#### Type Conversion

You can convert from one type to another with the `int()`, `float()`, and `complex()` methods:

```python
x = 1    # int  
y = 2.8  # float  
z = 1j   # complex  
  
#convert from int to float:  
a = float(x)  
  
#convert from float to int:  
b = int(y)  
  
#convert from int to complex:  
c = complex(x)  
  
print(a)  
print(b)  
print(c)  
  
print(type(a))  
print(type(b))  
print(type(c))
```

#### Random Number

Python does not have a `random()` function to make a random number, but Python has a built-in module called `random` that can be used to make random numbers:

```python
import random  
  
print(random.randrange(1, 10))
```


