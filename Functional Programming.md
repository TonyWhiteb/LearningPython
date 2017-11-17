# __Higher order function__

## map()

there are two variable in map()

1. function
2. Iterable
map() can apply the function on each iterable element

```python
>>> def f(x):
...     return x * x
...
>>> r = map(f, [1, 2, 3, 4, 5, 6, 7, 8, 9])
>>> list(r)
[1, 4, 9, 16, 25, 36, 49, 64, 81]
```
## reduce()

reduce() also has two variables
1. function
2. iterable

reduce() can apply function on a list and make cumulative calculations

```python
>>> from functools import reduce
>>> def fn(x, y):
...     return x * 10 + y
...
>>> reduce(fn, [1, 3, 5, 7, 9])
13579
```

## filter()

filter() can apply function on each element and return values are depended on the True or False

```python
def is_odd(n):
    return n % 2 == 1

list(filter(is_odd, [1, 2, 4, 5, 6, 9, 10, 15]))
# 结果: [1, 5, 9, 15]
```

the return value is a __Iterator__

## sorted()

```python
>>> sorted([36, 5, -12, 9, -21])
[-21, -12, 5, 9, 36]
```

based on key

```python
>>> sorted([36, 5, -12, 9, -21], key=abs)
[5, 9, -12, -21, 36]
```

#__Return Function__

## Closure

## lambda function

lambda function only can have one expression, and do not need to write return.

## Decorator

dynamically add function during running the code.

call a function and return a function.

```Python
def log(func):
    def wrapper(*args, **kw):
        print('call %s():' % func.__name__)
        return func(*args, **kw)
    return wrapper
```
```Python
@log
def now():
    print('2015-3-25')
```
result:
```Python
>>> now()
call now():
2015-3-25
```

log() is a decorator and return a function wrapper().

then call wrapeer() and return func(), which in this case is now()



now() still exist, but the variable ...

## Partial Function

simplify the call process

```Python
def int2(x, base=2):
    return int(x, base)
  >>> int2('1000000')
  64
  >>> int2('1010101')
  85  
```

```Python
>>> import functools
>>> int2 = functools.partial(int, base=2)
>>> int2('1000000')
64
>>> int2('1010101')
85
```
