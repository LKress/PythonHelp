# PythonHelp
Things i didn't knew about Python
---
Tilde operator (~) 
inverts things
E.g.: 
```df = df[~df.something.isin(df2.something)]```
After this line in df there will only be the "something" entries that are not in df2
```>> df
>> col1 col2 col3 something
   1    4    2    "A"
   7    2    5    "B"
   1    4    2    "B"
   9    3    6    "A"
   0    4    2    "C"```
   
```>> df2
>> col1 col2 col3 something
   1    3    2    "A"
   4    2    7    "D"
   1    9    3    "D"
   8    3    0    "A"
   2    1    5    "C"```
   
After the line

```df = df[~df.something.isin(df2.something)]```

df will look:

```>> df
>> col1 col2 col3 something
   7    2    5    "B"
   1    4    2    "B"```
