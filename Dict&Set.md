# __Dict__

__key - value__: get data based on the __key__

__One key__ only can have __one value__ or __overwrite__

### how to check if the key exist

#### in
```Python
>>> 'Thomas' in d
False
```

#### get
You can give the key __a value__ or return __None__
```Python
>>> d.get('Thomas')
>>> d.get('Thomas', -1)
-1
```
#### pop()

delete key and value also will be removed

### Comparison

A __List__ keeps __order__, __Dict__ and __Set__ don't

__Dict__ associates with each key __a value__, while __List__ and __Set__ just __contain__ values

__Set__ requires items to be hashable, __List__ doesn't

An object is __hashable__ if it has __a hash value__ which __never changes__ during its lifetime (it needs a __hash__() method), and can be compared to other objects (it needs an __eq__() method). Hashable objects which compare equal __must have the same hash value.__

__set__ forbids __duplicates__, __list__ does not

Checking for membership of a value in a __set__ (or __dict__, for keys) is blazingly __fast__

# __Set__

The only difference between __Set__ and __Dict__ is that set __doesn't have values__

### add()

### remove()


# __Hash__

__Str__ is __hashable__

```Python
>>> a = 'abc'
>>> a.replace('a', 'A')
'Abc'
>>> a
'abc'
```
