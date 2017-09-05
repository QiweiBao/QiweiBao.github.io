## There are some special rules in for loops.

### symbol `_` [1]:
It's common in Python to use `_` representing throwaway variables. Similar to use of `~` in MatLab.
However, since there are more use of `_` in Python like:
1. To hold the result of the last executed expression in an interactive interpreter session. This precedent was set by the standard CPython interpreter, and other interpreters have followed suit.
2. For translation lookup in i18n, as in code like: raise forms.ValidationError(_("Please enter a correct username"))
To avoid confliction, a double-underscore `__` is preferred by many people.

```
>>> a = b = 1
>>> for _ in range(10):
...     a , b = a + b, a
>>> print a, b
144 89
```

Reference:
[1]https://stackoverflow.com/questions/5893163/what-is-the-purpose-of-the-single-underscore-variable-in-python