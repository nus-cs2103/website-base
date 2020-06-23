#### Exercise : Get Head, Get Tail

Complete the functions as described below:
* `get_head(item_list)`: returns the first item of the list received as the `item_list` parameter.
* `get_tail(item_list)`: returns the last item of the list received as the `item_list` parameter.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def get_head(item_list):
  return # ADD CODE HERE

def get_tail(item_list):
  return # ADD CODE HERE

print(get_head([1, 2, 3]))
print(get_tail(['a', 2, 3.0]))
```
</span>
<span id="output">

```
1
3.0
```
</span>
</include>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def get_head(item_list):
  return item_list[0]
```

</panel>