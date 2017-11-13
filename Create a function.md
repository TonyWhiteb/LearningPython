# Basic

## Def

```python
def my_abs(x):
    if x >= 0:
        return x
    else:
        return -x
```

## Blank function

```Python
def nop():
    pass
```

__pass__ is a __placeholder__, and to make your codes continue to run.

## Return multiple values

```Python
>>> r = move(100, 100, 60, math.pi / 6)
>>> print(r)
(151.96152422706632, 70.0)
```
The return value is a __Tuple__

## Default value

```Python
def power(x, n=2):
    s = 1
    while n > 0:
        n = n - 1
        s = s * x
    return s
```
Set almost __unchanged variable__ a default value is a good practice.

__Default value__ must be a __unhashable value__!

```Python
def add_end(L=[]):
    L.append('END')
    return L

>>> add_end()
['END', 'END']
>>> add_end()
['END', 'END', 'END']
```

```Python
def add_end(L=None):
    if L is None:
        L = []
    L.append('END')
    return L

>>> add_end()
['END']
>>> add_end()
['END']
```

## Changeable variable

\* + variable name is a __changeable variable__

```Python
def calc(*numbers):
    sum = 0
    for n in numbers:
        sum = sum + n * n
    return sum
>>> calc(1, 2)
5
>>> calc()
0  
```
If your input is a __list or Tuple__

```Python
>>> nums = [1, 2, 3]
>>> calc(*nums)
14
```
## Key Word variable

a __extension__ of your function valuable

it is a __dict__

```Python
def person(name, age, **kw):
    print('name:', name, 'age:', age, 'other:', kw)
>>> extra = {'city': 'Beijing', 'job': 'Engineer'}
>>> person('Jack', 24, **extra)
name: Jack age: 24 other: {'city': 'Beijing', 'job': 'Engineer'}    
```

In this case, the value of kw dict is a __copy__ of extra dict, which means this operation will not change the value of extra dict.

## Naming Key Word Variable

\* Separator

```python
def person(name, age, *, city, job):
    print(name, age, city, job)

```

## Order

Required variable -> Default variable -> Changeable variable -> Naming Key Word variable -> Key Word variable

```Python
def f1(a, b, c=0, *args, **kw):
    print('a =', a, 'b =', b, 'c =', c, 'args =', args, 'kw =', kw)

def f2(a, b, c=0, *, d, **kw):
    print('a =', a, 'b =', b, 'c =', c, 'd =', d, 'kw =', kw)
>>> args = (1, 2, 3, 4)
>>> kw = {'d': 99, 'x': '#'}
>>> f1(*args, **kw)
a = 1 b = 2 c = 3 args = (4,) kw = {'d': 99, 'x': '#'}
>>> args = (1, 2, 3)
>>> kw = {'d': 88, 'x': '#'}
>>> f2(*args, **kw)
a = 1 b = 2 c = 3 d = 88 kw = {'x': '#'}    
```
