### Booleans

**The `bool` data type is used to represent <tooltip content="i.e. true/false values">_boolean_ values</tooltip>**. They are useful when the program execution needs to vary based on a certain condition %%&nbsp;e.g., print 'old' if age is greater than 100.%%

The `bool` data type can hold only two values `True` and `False` (case sensitive).
```python
>>> type(True)
<class 'bool'>

>>> type(False)
<class 'bool'>

>>> type('True')
<class 'str'>

>>> type(true)
...
NameError: name 'true' is not defined
```

You can **use the comparison _operators_ to create an expression that evaluate to a boolean result**.

Operator | Meaning
:------: | -------
`==` | Equal to (different from the assignment operator `=`)
`!=` | Not equal to
`<` | Less than
`>` | Greater than
`<=` | Less than or equal to
`>=` | Greater than or equal to

{{ icon_example }} Here are some examples

```python
print('hello' == 'Hello') # False
print('dog' != 'cat') # True
print(True == True) # True
print(True != False) # True
print(42 == 42.0) # True (they are different types of numbers, but of same value)
print(42 == '42') # False
print(42 == int('42')) # True
print(20 > 10) # True
```

In contrast, **_boolean operators_ (`and`, `or` and `not`) work only on boolean values**. Here is how they work.

<div class="container">
  <div class="row">
    <div class="col-sm">
<markdown>
Expression | Result
---------- | ------
`True` **`and`** `True` | `True`
`True` **`and`** `False` | `False`
`False` **`and`** `True` | `False`
`False` **`and`** `False` | `False`
</markdown>
    </div>
    <div class="col-sm">
<markdown>
Expression | Result
---------- | ------
`True` **`or`** `True` | `True`
`True` **`or`** `False` | `True`
`False` **`or`** `True` | `True`
`False` **`or`** `False` | `False`
</markdown>
    </div>
    <div class="col-sm">
<markdown>
Expression | Result
---------- | ------
**`not`** `True` | `False`
**`not`** `False` | `True`
</markdown>
    </div>
  </div>
</div>

You can mix the two types of operators. Some examples below:

```python
result = (2 > 5) or (10 < 20) # True
result = (2 == 2) and (3 != 3) # False
```

<panel type="seamless" header="%%{{ icon_video }} Booleans%%">

<iframe width="560" height="315" src="https://www.youtube.com/embed/4XA9CKJJbr4?rel=0&showinfo=0&start=65&version=3" frameborder="0" allowfullscreen></iframe>

</panel>
