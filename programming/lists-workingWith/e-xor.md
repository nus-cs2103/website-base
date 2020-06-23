#### Exercise : XOR

%%{{ icon_info }} In case you didn't know: _XOR_ (short for eXclusive OR) is a logical operation, when applied to two booleans, that outputs `True` only when inputs differ (one is `True`, the other is `False`)%%

Complete the functions as described below:
* `xor(list1, list2, item)`: returns `True` if `item` is in ++only++ one of the two lists `list1` and `list2`. i.e., returns `False` if the `item` is absent from both lists or present in both lists.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def xor(list1, list2, item):
  return

print(xor(['a','b'], ['a', 'c'], 'a'))
print(xor(['a','b'], ['a', 'c'], 'b'))
print(xor(['a','b'], ['a', 'c'], 'c'))
print(xor(['a','b'], ['a', 'c'], 'd'))
```
</span>
<span id="output">

```
False
True
True
False
```
</span>
</include>


<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
return (item in list1 and item not in list2) or (...)
```
</panel>