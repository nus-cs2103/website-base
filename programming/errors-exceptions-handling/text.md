### Handling Exceptions

**Errors detected during execution are called _exceptions_.** Even if the code is syntactically correct, it may cause an error during execution. Python _<tooltip content="_throw_ and _raise_  are two terms used to describe an exception being encountered">throws/raises</tooltip>_ different types of exceptions; the type of exception used depends on the tye nature of the error.

<box>

{{ icon_example }} The code below raises an exception when it attempts to divide a number by `0`. The type of the exception raised is `ZeroDivisionError`, as mentioned in the last line of the error message.

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
def divide(number, divisor):
  print('Starting calculation')
  result = number/divisor
  print(number, '/', divisor, '=', result)
  print('Calculation over!........')

divide(50, 5)
divide(3, 0)
```
</span>
<span id="output">

```
Starting calculation
50 / 5 = 10.0
Calculation over!........

Starting calculation
Traceback (most recent call last):
  File "python", line 9, in <module>
  File "python", line 4, in divide
ZeroDivisionError: division by zero
```
</span>
</include>

</box>

It is not desirable for programs to 'crash' every time an exception occurs. You can **use the `try-except` syntax to specify how to handle exceptions**. The `try` clause contains the code that can possibly raise an exception while the `except` clause contains the code that handles the exception.

<box>

{{ icon_example }} The code below specifies what to do if the `ZeroDivisionError` is raised, thereby avoiding a program crash in such an event.

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
def divide2(number, divisor):
  print('Starting calculation')
  try:
    result = number/divisor
    print(number, '/', divisor, '=', result)
  except ZeroDivisionError:
    print('Cannot divide by zero')
  print('Calculation over!........')

divide2(3, 0)
divide2(3, 1.5)
```
</span>
<span id="output">

[<a target="_blank" href="https://goo.gl/rc8X9h">visualize</a>]<br>
```
Starting calculation
Cannot divide by zero
Calculation over!........

Starting calculation
3 / 1.5 = 2.0
Calculation over!........
```
</span>
</include>

</box>

When the code in a `try` clause raises an error, the program execution immediately moves to the code in the `except` clause, provided the exception that happened matches the exception the `except` clause is supposed to _<tooltip content="_Catch_ is term often used to describe a clause that respondes to a specific exception.">catch</tooltip>_. After running the code in the `except` clause, the execution continues as normal. 

If the exception does not match the `except` clause, the program crashes.

<box>

{{ icon_example }} The code below crashes because the actual exception %%(caused by passing a string when an foloating point number is expected)%% does not match the specified exception `ZeroDivisionError`.

<include src="inputOutput.md" var-align="top" boilerplate>
<span id="input">

```python
divide2(5, 'abc')
```
</span>
<span id="output">

```
Starting calculation
Traceback (most recent call last):
  File "python", line 24, in <module>
  File "python", line 16, in divide2
TypeError: unsupported operand type(s) for /: 'int' and 'str'
```
</span>
</include>

</box>

**You can specify multiple `except` clauses**, one for each type of exception expected.

<box>

{{ icon_example }} The code below handles two types of exceptions: `ZeroDivisionError` and `ValueError`.

{{ icon_tip }} The `ValueError` is raised when the string `abc` is being converted to a float using `float(divisor)`.

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
def divide3(number, divisor):
  print('Calculating', number, '/', divisor)
  try:
    result = float(number)/float(divisor)
    print(number, '/', divisor, '=', result)
  except ZeroDivisionError:
    print('Cannot divide by zero')
  except ValueError:
    print('Cannot divide non-numbers')
  print('Calculation over!........')

divide3(3, 0)
divide3(3, 'abc')
```
</span>
<span id="output">

```
Calculating 3 / 0
Cannot divide by zero
Calculation over!........

Calculating 3 / abc
Cannot divide non-numbers
Calculation over!........
```
</span>
</include>


</box>

**It is possible to specify multiple exception types in one `except` clause.**

<box>

{{ icon_example }} The code below handles both `ZeroDivisionError` and `ValueError` in the same `except` clause.

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
def divide4(number, divisor):
  print('Calculating', number, '/', divisor)
  try:
    result = float(number)/float(divisor)
    print(number, '/', divisor, '=', result)
  except (ZeroDivisionError, ValueError):
    print('Incorrect inputs')
  print('Calculation over!........')

divide4(3, 0)
divide4(3, 'abc')
```
</span>
<span id="output">

```
Calculating 3 / 0
Incorrect inputs
Calculation over!........

Calculating 3 / abc
Incorrect inputs
Calculation over!........
```
</span>
</include>

</box>

[`IndexError`](https://docs.python.org/3/library/exceptions.html#IndexError) is an exception thrown when you try to access an index (e.g., when reading values form a list) that does not exist.

<box>

{{ icon_example }} In this example, calling `get_head` on an empty list causes an `IndexError`.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def get_head(items):
  try:
    return items[0]
  except IndexError:
    return 'List too short'

print(get_head([]))
```
</span>
<span id="output">

```
List too short
```
</span>
</include>

</box>

It is also possible to **use `except Exception` to catch any kind of exception**. However, that practice is discouraged. 

<box>

{{ icon_example }} The code below handles both `ZeroDivisionError` and `ValueError` in the same `except` clause.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def get_head2(items):
  try:
    return items[0]
  except Exception:
    return 'Something wrong'

print(get_head2(2))
```
</span>
<span id="output">

```
Something wrong
```
</span>
</include>

</box>

<include src="tryYourOwn.md" boilerplate var-program="errors-exceptions-handling" />

:paperclip: **Resources**:
* [Python built-in exceptions](https://www.tutorialspoint.com/python/standard_exceptions.htm)

<include src="exercisePanel.md" boilerplate var-title="Enter Integer" var-file="e-enterInteger.md" />