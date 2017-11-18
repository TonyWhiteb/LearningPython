# Package

mycompany

 ├─ web

 │  ├─ \_\_init__.py

 │  ├─ utils.py

 │  └─ www.py

 ├─ \_\_init__.py

 ├─ abc.py

 └─ xyz.py

 \_\_init__.py is very important, otherwise python will not know this is a package.

 \_\_init__.py can be blank or not.

 ```python
 #!/usr/bin/env python3
# -*- coding: utf-8 -*-

' a test module '

__author__ = 'Michael Liao'

import sys

def test():
    args = sys.argv
    if len(args)==1:
        print('Hello, world!')
    elif len(args)==2:
        print('Hello, %s!' % args[1])
    else:
        print('Too many arguments!')

if __name__=='__main__':
    test()
 ```
# important
 ```python
 if __name__=='__main__':
     test()
 ```
 When we run the py file, python interpreter will set \_\_name\_\_ as \_\_main__.

 if you use this py file as a module in somewhere, this if sentence will be invalid.

# __Scope__

## Public

Public variable can be referred directly.

## __\_\_xxx\_\___

Special variables have special use.

## Private

\_xxx and \_\_xxx are Private, and can not be referred directly.

```python
def _private_1(name):
    return 'Hello, %s' % name

def _private_2(name):
    return 'Hi, %s' % name

def greeting(name):
    if len(name) > 3:
        return _private_1(name)
    else:
        return _private_2(name)
```
