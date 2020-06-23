#### Exercise : Expand to Fill

Complete the functions as described below:
* `expand_to_fill(item_list, length)`: returns a list containing a total of `length` items, where the items are repetitions of the items in the `item_list`.

{{ icon_tip }} hints
* full_repetitions_needed = `length` `//` length_of_item_list
* return `item_list` `*` full_repetitions_needed `+` portion_of_item_list
 

```python
def expand_to_fill(item_list, length):
  return  # REPLACE WITH YOUR CODE

meals = ['Rice', 'Bread', 'Noodles']
print(expand_to_fill(meals, 5))
print(expand_to_fill(meals, 7))
```
{{ icon_output }}
  
```
['Rice', 'Bread', 'Noodles', 'Rice', 'Bread']
['Rice', 'Bread', 'Noodles', 'Rice', 'Bread', 'Noodles', 'Rice']

```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
  ...
  temp = item_list * (length//len(item_list))
  shortfall = length - len(temp)
  if shortfall > 0:
    result = temp + item_list[:shortfall]
  ...
```
</panel>