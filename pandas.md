# Pandas Help

### Select specific rows of a dataframe
One condition:
```python
df.loc[df['column1'] > 6]
```
More conditions (mind the brackets):
```python
df.loc[(df['column1'] > 6) & (df['column2'] < 6)]
```
