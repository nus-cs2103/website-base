#### Exercise : Is Even-Integer in Range

<tip-box> 

{{ icon_important }} This exercise has a long description because it explains how the given code is structured. It is important for you to learn how to break down code into smaller functions like the ones given in this exercise.

</tip-box>

The function given below checks if a given input is an even integer in a given range.

```python
def check(number, start, end):
  print(number, 'is an int in range', start, '-', end, '?', is_even_int_in_range(number, start, end))
```

Some example inputs and outputs are given below:  
```python
check(3, 'y', 'z') # False (3 is not even)
check(2, 3.4, 5)
check(2, 3, [])
check(2, 5, 1)
check(2, 5, 5)
check(3, 1, 5)
check(4, 1, 4) # False ( range 1 to 4 excludes 4)
check(4, 1, 5)
```
{{ icon_output }}
```
x is an int in range y - z ? Value error: x is not an integer
3 is an int in range y - z ? No
2 is an int in range 3.4 - 5 ? Value error: 3.4 is not an integer
2 is an int in range 3 - [] ? Value error: [] is not an integer
2 is an int in range 5 - 1 ? Value error: end is smaller than start
2 is an int in range 5 - 5 ? No
3 is an int in range 1 - 5 ? No
4 is an int in range 1 - 4 ? No
4 is an int in range 1 - 5 ? Yes
```

Note how the `check` function uses an `is_even_int_in_range` functions whose code and the behavior are given below. 

**`is_even_int_in_range(number, start, end)`**:
* Returns `'Yes'` if `number` is an even integer in the range `start` to `end`. Returns `'No'` otherwise.
* Returns an error message if any of the inputs are incorrect.
* Code:
  ```python
  def is_even_int_in_range(number, start, end):
    try:
      if is_even_int(number) and is_in_range(number, start, end):
        return 'Yes'
      else:
        return 'No'
    except ValueError as e:
      return 'Value error: ' + str(e)
  ``` 

Note how the above function uses two other functions `is_even_int` and `is_in_range` given below:

**`is_even_int(number)`**:
* Returns `True` if the `number` is an even integer. `False` otherwise.
* Raises a `ValueError` if the `number` is not an integer.
* Code:
  ```python
  def is_even_int(number):
    confirm_is_int(number)
    return int(number)%2 == 0
  ```

**`is_in_range(number, start, end)`**: 
* Returns `True` if the `number` is in the range `start` to `end` (==including `start` but excluding `end`==, as per how Python define _ranges_). `False` otherwise.
* Raises a `ValueError` if the `number` is not an integer or `start` and `end` do not specify a range correctly.
* Code: 
  ```python
  def is_in_range(number, start, end):
    confirm_is_int(number)
    confirm_range_correct(start, end)
    return number >= start and number < end
  ```
Note how the above two functions use two other functions `confirm_is_int` and `confirm_range_correct`. Their expected behavior and partial code is given below. **Your job is to complete those two functions**.

**`confirm_is_int(number)`**: 
* Raises a `ValueError` if the `number` is not an integer.
* Partial code:
  ```python
  def confirm_is_int(number):
    pass # ADD YOUR CODE HERE!
  ```
* {{ icon_tip }} You can use the `type(value) is type_name` and `type(value) is not type_name` to check if a `value` is of type `type_name`<br>
  e.g., `type('x') is not float` evaluates to `True` because `'x'` is not a `float`.<br>
  [[more examples ...](https://www.poftut.com/python-type-function-examples/)]
  
**`confirm_range_correct(start, end)`**:
* Raises a `ValueError` if `end` or `start` are not integers. This behavior is already implemented by the code given below, using two calls to the `confirm_is_int` function.
* Raises a `ValueError('end is smaller than start')` if `end` is smaller than `start`. You need to implement this behavior.
* Partial code:
  ```python
  def confirm_range_correct(start, end):
    confirm_is_int(start)
    confirm_is_int(end)
    # ADD YOUR CODE HERE!
  ```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def confirm_is_int(number):
  if type(number) is not int:
    raise ValueError(str(number) + ' is not an integer')
```

</panel>