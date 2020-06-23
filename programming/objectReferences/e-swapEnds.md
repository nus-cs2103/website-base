#### Exercise : Swap Ends

Complete the functions as described below:
* `swap_ends(item_list)`: swaps the first and the last items of the `item_list`. Note that the function should modify the given `item_list` list, not return a new list.  

Notes:
* You can follow the example of `set_head(item_list, new_head)` function which modifies the given `item_list` by setting its first element to `new_head`.
* `pass` is a dummy statement that does nothing. We use it here because Python does not accept empty functions. You should replace it with your own implementation of the function.

<table>
<tr>
  <td>

```python
def set_head(item_list, new_head):
  item_list[0] = new_head
  
def swap_ends(item_list):
  pass # REPLACE THIS WITH YOUR CODE

pets = ['cat', 'fish', 'dog', 'rock']
set_head(pets, 'parrot')
print(pets)
swap_ends(pets)
print(pets)
```
  </td>
  <td><br><br><br><br><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br><br><br><br><br>
  
```
['parrot', 'fish', 'dog', 'rock']
['rock', 'fish', 'dog', 'parrot']
```
  </td>
</tr>
</table>