### Raising Exceptions

**You can `raise` an exception yourself to indicate an error**.

<box>

{{ icon_example }} The `get_body(items)` function below raises an exception when it receives a list that has fewer than 3 items. That exception is 'caught' and handled by the `hide_ends(items)` function. <br>
{{ icon_tip }} Also note how an `except` clause can assign a name to the exception using `as temporary_name` (as done by `except ValueError as e:`) so that the exception object can be referenced later (as done in `print('Cannot hide ends', str(e))`)

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def get_body(items):
  if len(items) < 3:
    raise ValueError('Not enough items')

  return items[1:-1]

def hide_ends(items):
  try:
    body = get_body(items)
    print(['_'] + body + ['_'])
  except ValueError as e:
    print('Cannot hide ends:', str(e))

hide_ends([0, 1])
hide_ends([0, 1, 2, 3, 4])
```
</span>
<span id="output">

[<a target="_blank" href="https://goo.gl/tsteqe">visualize</a>]<br>
```
Cannot hide ends: Not enough items
['_', 1, 2, 3, '_']
```
</span>
</include>

</box>

**It is also possible to catch an exception, do something, and then raise it again** so that the exception propagates to the caller.

<box>

{{ icon_example }} The code `hide_ends2(items)` function below catches the `ValueError` exception, prints an error message, and raises it again so that the code that called the function can catch the exception again. Also note how the line `hide_ends2([0, 1, 2, 3, 4])` is never executed due to the exception raised by the line just above it.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def hide_ends2(items):
  try:
    body = get_body(items)
    print(['_'] + body + ['_'])
  except ValueError as e:
    print('Cannot hide ends:', str(e))
    raise

try:
  hide_ends2([0])
  hide_ends2([0, 1, 2, 3, 4])
except ValueError as e:
  print('hide_ends2 failed:', str(e))
```
</span>
<span id="output">

[<a target="_blank" href="https://goo.gl/EGkxAW">visualize</a>]<br>

```
Cannot hide ends: Not enough items
hide_ends2 failed: Not enough items
```
</span>
</include>

</box>

<include src="tryYourOwn.md" boilerplate var-program="errors-exceptions-raising" />

Here are some commonly used built-in exceptions ([full list](https://docs.python.org/3/library/exceptions.html#concrete-exceptions)) you can raise/handle in your code:
* `IndexError`: Indicates an index of a sequence (e.g., a list) is out of range.
* `RuntimeError` : Indicates an error that does not fall under any other category.
* `ValueError`: Indicates when a function gets argument of correct type but improper value.
* `ZeroDivisionError` : Indicates an attempt to divide by zero.

It is also possible to define your own _user-defined exceptions_ but that requires more advanced programming techniques. It will be covered elsewhere.

<include src="exercisePanel.md" boilerplate var-title="Is Even-Integer in Range" var-file="e-isEvenIntegerInRange.md" />
<include src="exercisePanel.md" boilerplate var-title="Flexible Word Game" var-file="e-flexibleWordGame.md" />