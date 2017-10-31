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
```
