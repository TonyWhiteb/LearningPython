# __Slicing__

```python
>>> L = ['Michael', 'Sarah', 'Tracy', 'Bob', 'Jack']
>>> L[0:3]
['Michael', 'Sarah', 'Tracy']
```
```L[0:3]``` index start from 0 to 3 not including 3

```L[-1]``` return the last element in this list.

__Tuple__ is kind of list, so __Tuple__ can be sliced

__Str__ can also be sliced

```python
>>> 'ABCDEFG'[:3]
'ABC'
>>> 'ABCDEFG'[::2]
'ACEG'
```

#__Iteration__

if this is an iterable data, it can be iterated

## Check if it is iterable

```python
>>> from collections import Iterable
>>> isinstance('abc', Iterable)
True
>>> isinstance([1,2,3], Iterable)
True
>>> isinstance(123, Iterable)
False
```

## enumerate()

return the index and the elements

```python
>>> for i, value in enumerate(['A', 'B', 'C']):
...     print(i, value)
...
0 A
1 B
2 C
```

# __List Comprehensions__

List comprehensions can simplify your query!

```python
>>> L = []
>>> for x in range(1, 11):
...    L.append(x * x)
...
>>> L
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

```python
>>> [x * x for x in range(1, 11)]
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

## with conditions

```python
>>> [x * x for x in range(1, 11) if x % 2 == 0]
[4, 16, 36, 64, 100]
```

## Two dimensions loop

```python
>>> [m + n for m in 'ABC' for n in 'XYZ']
['AX', 'AY', 'AZ', 'BX', 'BY', 'BZ', 'CX', 'CY', 'CZ']
```

#__Generator__

The storage of list is limited, so you need to create a generator if you only needs some values of a big list.

## Use ()

```python
>>> L = [x * x for x in range(10)]
>>> L
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
>>> g = (x * x for x in range(10))
>>> g
<generator object <genexpr> at 0x1022ef630>
```
## Use yield

```python
def fib(max):
    n, a, b = 0, 0, 1
    while n < max:
        print(b)
        a, b = b, a + b
        n = n + 1
    return 'done'
```

```python
def fib(max):
    n, a, b = 0, 0, 1
    while n < max:
        print(b)
        t = (b, a + b) # t是一个tuple
        a = t[0]
        b = t[1]
        n = n + 1
    return 'done'
```

```python
def fib(max):
    n, a, b = 0, 0, 1
    while n < max:
        yield b
        a, b = b, a + b
        n = n + 1
    return 'done'
```

Generator stop on 'yield' and restart on 'yield' too

```python
def odd():
    print('step 1')
    yield 1
    print('step 2')
    yield(3)
    print('step 3')
    yield(5)
```
result:
```python
>>> o = odd()
>>> next(o)
step 1
1
>>> next(o)
step 2
3
>>> next(o)
step 3
5
>>> next(o)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
StopIteration
```

#__Iterator__

Iterator can be called and return values continuously.

Iterator data type is kind of data stream with order, and we can not know how long it is until get the last one.
