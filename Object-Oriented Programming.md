# Class

```python
class Student(object):
    pass
```

Class is abstract.

All classes are inherited from object class.

##\_\_inti\_\_

we can use \_\_inti\_\_ to add some required attributes to your class.

```python
class Student(object):

    def __init__(self, name, score):
        self.name = name
        self.score = score
```
self means the instance itself.

## Method

```python
class Student(object):

    def __init__(self, name, score):
        self.name = name
        self.score = score

    def print_score(self):
        print('%s: %s' % (self.name, self.score))
```

we can use the method in our class directly.

# Access Restriction

Outside code can still change the attributes of an instance in a class.

```python
>>> bart = Student('Bart Simpson', 59)
>>> bart.score
59
>>> bart.score = 99
>>> bart.score
99
```
If you want the access restriction, you can add "\_\_" before the variable and make this variable be a private variable in the class.

```python
class Student(object):

    def __init__(self, name, score):
        self.__name = name
        self.__score = score

    def print_score(self):
        print('%s: %s' % (self.__name, self.__score))
```

If you want get the private variable:
```python
class Student(object):
    ...

    def get_name(self):
        return self.__name

    def get_score(self):
        return self.__score
```

if you want to change the value of private variable:

```python
class Student(object):
    ...

    def set_score(self, score):
        self.__score = score
```
```python
class Student(object):
    ...

    def set_score(self, score):
        if 0 <= score <= 100:
            self.__score = score
        else:
            raise ValueError('bad score')
```
