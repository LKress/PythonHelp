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
### Change string values complete column
Changes all the column entries, so that a - after a digit [0-9] gets replaced by a /.
The lambda gets the first occurence of this regex and takes the first char ([0]).
```python
repl = lambda m: m.group(0)[0] + "/"
data["col_name"] = data["col_name"].str.replace(r'[0-9]-', repl)
```
