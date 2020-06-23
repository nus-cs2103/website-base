#### Exercise : First Quarter

Complete the functions as described below:
* `print_dates()`: prints the dates of the first four months of the year, in the format given in the sample output.

* You ==must use the given lists `months` and `lengths`== in your solution.
* You can use the functions given below:
  * `generate_number_string(start, end)`: Returns a string containing integers from `start` to `end` (not inclusive), separated by space.<br>
    e.g., `generate_number_string(5, 10)` → `'5 6 7 8 9'`
 

```python
def generate_number_string(start, end):
  number_string = ''
  for i in range(start, end):
    number_string = number_string + ' ' + str(i)
  return number_string
  
def print_dates():
  months = ['Jan', 'Feb', 'Mar', 'Apr'] # months of the first quarter
  lengths = [31, 28, 31, 30] # number of days in each month of the first quarter
  # ADD CODE HERE

print_dates()
```
{{ icon_output }}
  
```
Jan: 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31
Feb: 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28
Mar: 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31
Apr: 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
  ...
  for i, month in enumerate(months):
      print( ... + generate_number_string(1, lengths[i]+1))

```
</panel>