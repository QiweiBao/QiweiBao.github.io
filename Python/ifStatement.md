## In Python, there are some difference on True or False judgement.

### Difference of `is` and `==`:
`==` compares the value while `is` compares the address of the value. Thus, (ob1 is ob2) is equal to (id(ob1) == id(ob2)).

```
Example:
>>> a = [12]
>>> b = [12]
>>> id(a)
4327524472
>>> id(b)
4327570104
>>> a == b
True
>>> a is b
False
```

* In Python, objects are divided as mutable and immutable.

	`tuple`, `number` and `string` are regarded as immutable object, where their addresses will not change.
	```
	Example:
	>>> a = 12
	>>> b = 12
	>>> id(a)
	140729425876880
	>>> id(b)
	140729425876880
	```

	However, if there are arithmetic operation on the value, their addresses will change.
	```
	Example:
	>>> a = 12
	>>> id(a)
	140729425876880
	>>> a += 1
	>>> id(a)
	140729425876856
	 ```

	Other objects are mutable objects. Thus, operations on them will not change their addresses.
	```
	Example:
	>>> a = [1, 2]
	>>> id(a)
	4300247408
	>>> a.append(3)
	>>> id(a)
	4300247408
	```
* Problems may cause:

	For the mutable objects, if users hope to change one object without influence other objects, sometimes more storage is needed.
	```
	Example:
	>>> a = [1, 2]
	>>> b = a
	>>> b[0] = 2
	>>> a
	[2, 2]
	```

### Difference of judge if a variable is equal to None:
In Python, `None`, `False`, `""`, `0`, `[]`, `{}`, `()` are regarded as False. However, this doesn't means these objects directly equal to False.
	```
	Example:
	>>> a = []
	>>> not a
	True
	>>> a == False
	False
	```

