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
