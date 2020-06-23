#### Exercise : Enter Integer

The code below assumes the entered string will always represent an integer. 

```python
value = input('Input an integer:')
print('You entered', value)
```

However, users may not follow that assumption. If the user were to enter a non-integer string, the program crashes. To avoid such crashes, programs need to do _input validation_ i.e., perform checks on inputs to ensure their validity. 

Update the above code so that it accepts integers only, and produces the behavior given below.

```
Input an integer: x
That is not an integer, try again
Input an integer: 5.5
That is not an integer, try again
Input an integer: 6
You entered 6
```

<panel type="seamless" header="%%:bulb: Hint%%">

* [The `int(s)` function](https://www.programiz.com/python-programming/methods/built-in/int) raises a `ValueError` when the string `s` does not represent an integer.
* You can use a `while True` loop to repeatedly ask for an input until the user enters an integer.
</panel>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
while True:
  try:
    value = int(input('Input an integer:'))
    # YOUR CODE HERE! print? break? continue?
  except ValueError:
    # YOUR CODE HERE!
    
print('You entered', value)
```

</panel>