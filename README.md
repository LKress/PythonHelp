# PythonHelp

Things I didn't know or find interesting. The same for pandas can be found here: https://github.com/LKress/PythonHelp/pandas.md
Helpful things in python
---

### Tilde operator (~) 

inverts things
E.g.: 
```python
df = df[~df.something.isin(df2.something)]
```
After this line in df there will only be the "something" entries that are not in df2
```
>> df
>> col1 col2 col3 something
   1    4    2    "A"
   7    2    5    "B"
   1    4    2    "B"
   9    3    6    "A"
   0    4    2    "C"
```
   
```
>> df2
>> col1 col2 col3 something
   1    3    2    "A"
   4    2    7    "D"
   1    9    3    "D"
   8    3    0    "A"
   2    1    5    "C"
```
   
After the line

```python
df = df[~df.something.isin(df2.something)]
```

df will look:

```
>> df
>> col1 col2 col3 something
   7    2    5    "B"
   1    4    2    "B"
```

### vars() method

returns a dict of an object
E.g.:
```python
class Test_vars:
   def __init__(self, a = 3, b = 5):+
      self.a = a
      self.b = b
      
object = Test_vars()
print(vars(object))
```

returns:
```
{'b': 5, 'a': 3}
```

### enumerate() method
Allows to loop over something with an counter
E.g.:
```python
for counter, value in enumerate(something_iterable):
   print(counter, value)
```
This will return the index and the value of the iterable object.
It's possible to set a starting index. Just insert a second argument to enumerate (int).

### Calculation with boolean value
Its allowed to add a number to a boolean value.
`False` stands for 0 `True` for 1:
E.g.:
```python
erg = True + 1
print(erg)
``` 
returns 2.

Also good for:
```python
erg = ( 5 > 6 ) + 1
print(erg)
```
will return 1.


### Method parametres
In the header of a method the parametres are defined. Their type or default parameter can be defined.

E.g.:
```python
def method(param1, param2: type, param3=DefaultValue):
``` 

### Accessing dictionary data
The method items() returns the items (key and value tuples) stored inside the dictionary.
```python
dictionary = { 'key1' : 1, 'key2' : 2, 'key3' : 3 }
print(dictionary.items())
```
will return:
```
dict_items([('key1',1), ('key2',2), ('key3',3)]) 
```

The method values() returns the values stored inside the dictionary.
```python
dictionary = { 'key1' : 1, 'key2' : 2, 'key3' : 3 }
print(dictionary.values())
```
will return:
```
dict_values([1, 2, 3]) 
```

To access the values one after another use a for loop:
```python
for key, value in dictionary.items():
   print(key)
   print(value)
```
will return:
```
key1
1
key2
2
key3
3
```

Style tips
---

If a method has more than two arguments define them one each column. 
E.g.:

```python
def method(
   arg1,
   arg2,
   arg3: int,
   arg4 = None,
   arg5: int = 1,
):
   <method body>
```
