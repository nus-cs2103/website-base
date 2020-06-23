#### Exercise : Delete Head, Delete Tail

Complete the functions as described below:
* `delete_head(item_list)`: deletes the first item in the list passed as `item_list` parameter.
* `delete_tail(item_list)`: deletes the last item in the list passed as `item_list` parameter.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def delete_head(item_list):
  pass # REPLACE THIS WITH YOUR CODE

def delete_tail(item_list):
  pass # REPLACE THIS WITH YOUR CODE

letters = ['a', 'b', 'c']
print(letters)
delete_head(letters)
print(letters)
delete_tail(letters)
print(letters)
```
</span>
<span id="output">

```
['a', 'b', 'c']
['b', 'c']
['b']
```
</span>
</include>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def delete_head(item_list):
  del item_list[0]
```

</panel>