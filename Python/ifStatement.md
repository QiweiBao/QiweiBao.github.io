## In Python, there are some difference on `if` statmement.

### Difference of `is` and `==`:
`==` compares the value while `is` compares the address of the value.

```
Example:
>>> a = [12]
>>> b = [12]
>>> id(a)
4327524472
>>> id(b)
4327570104
```

* In Python, objects are divided as mutable and immutable.
	`tuple`, `number` and `string` are regarded as immutable object, where their id will not change.
	```
	Example:
	>>> a = 12
	>>> b = 12
	>>> id(a)
	140729425876880
	>>> id(b)
	140729425876880
	```

	However, if there are arithmetic operation on the value, their id will change.
	```
	Example:
	>>> a = 12
	>>> id(a)
	140729425876880
	>>> a += 1
	>>> id(a)
	140729425876856
	 ```


### Difference of judge if a variable is equal to None:
In Python, `None`, `False`, `""`, `0`, `[]`, `{}`, `()` are all equal to False.

