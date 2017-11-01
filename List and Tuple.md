# List

list is __an array with index__.

Using __len()__ for a list can return __the number of elements__ in this list.

Index in a list begins with __'0'__

The last index is __len(list_name)-1__ or '__-1__'

__append()__: add a new element to the __end__ of the list.

```Python
>>> classmates.append('Adam')
>>> classmates
['Michael', 'Bob', 'Tracy', 'Adam']
>>> classmates.insert(1, 'Jack') # add into specific position
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy', 'Adam']
```

__pop()__: remove the element in the __end__ of the list

```Python
>>> classmates.pop()
'Adam'
>>> classmates
['Michael', 'Jack', 'Bob', 'Tracy']
>>> classmates.pop(1) #remove specific position element
'Jack'
>>> classmates
['Michael', 'Bob', 'Tracy']
>>> classmates[1] = 'Sarah' #replace an element
>>> classmates
['Michael', 'Sarah', 'Tracy']
```

The elements in a list could be __different__ data type

```Python
>>> L = ['Apple', 123, True]
>>> s = ['python', 'java', ['asp', 'php'], 'scheme']
>>> len(s)
4
```
# Tuple

Tuple is similar to list, but the only difference is that tuple __cannot be changed__!

Define one element Tuple
```Python
>>> t = (1,)
>>> t
(1,)
```
"changeable" Tuple
```Python
>>> t = ('a', 'b', ['A', 'B'])
>>> t[2][0] = 'X'
>>> t[2][1] = 'Y'
>>> t
('a', 'b', ['X', 'Y'])
```
The __list__ in the tuple could be changed.
