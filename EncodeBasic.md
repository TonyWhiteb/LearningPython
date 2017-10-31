##Encode
 1 byte = __8__ bit

 the maximum number of 1 byte is __255__

 the maximum number of 2 bytes is __65535__

 __ASCII__ encode only contains __letters, numbers and some symbols__

 __Unicode__ uses __two__ bytes to represent __one__ character

"A" :(Unicode) __00000000 01000001__(ASCII) __01000001__

If you write in English but use Unicode to encode, the storage space will be __twice__.

__UTF-8__ is used to save storage space of __Unicode__

Actually, __ASCII__ is part of __UTF-8__

![Notebook](LearningPython/image/2.png )
![Server](LearningPython/image/3.png )

##Encode in Python

Python 3 uses __Unicode__ to encode

__ord()__ convert a string to __Unicode__

__chr()__ is the inverse of __ord()__

When Data is transfering on Internet or save into driver, the data will be converted to __bytes__

```Python
x = b'ABC'
x = 'ABC'
```

 Although the results are the same, __one character is one byte__ in bytes

 String can convert to specific encoding using __encode()__

 ``` Python
 >>> 'ABC'.encode('ascii')
b'ABC'
>>> '中文'.encode('utf-8')
b'\xe4\xb8\xad\xe6\x96\x87'
>>> '中文'.encode('ascii')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
UnicodeEncodeError: 'ascii' codec can't encode characters in position 0-1: ordinal not in range(128)
 ```

 __decode()__ is the inverse of __encode()__

__len()__
```Python
>>> len('ABC')
3
>>> len('中文')
2
>>> len(b'ABC')
3
>>> len(b'\xe4\xb8\xad\xe6\x96\x87')
6
>>> len('中文'.encode('utf-8'))
6
```

When Python interpreter wants to read the codes in utf-8
```Python
#!/usr/bin/env python3
# -*- coding: utf-8 -*-
```
The first line is to tell Linux/OS X that this is a executable Python codes.
The second line is to tell Python interpreter read these codes in UTF-8

##Placeholder

__%d__: integer

__%f__: Float

__%s__: String

__%x__: Hexadecimal integer
