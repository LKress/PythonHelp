# Pandas Help

### Select specific rows of a dataframe
One condition:
```python
df.loc[df['column1'] > 6]
```
Multiple conditions (mind the brackets arround the conditions):
```python
df.loc[(df['column1'] > 6) & 
        (df['column2'] < 6) &
        (df['column3'].str.match("test")]
```
