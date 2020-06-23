#### Exercise : Get Part

Complete the `get_part(text, index)` function given below, to behave as follows:
1. Split `text` using `|` as the delimiter
1. Return the part indicated by the `index`

The return value should not have leading/trailing spaces.

```python
def get_part(text, index):
  #pass # REPLACE WITH YOUR CODE
```

Example usage:
<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
print(get_part(' John Doe | Male |    X', 0))
print(get_part('John Doe | Male |    X', 2))
print(get_part('Dog|Cat', 0))
```
</span>
<span id="output">

```
John Doe
X
Dog
```
</span>
</include>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
return text.split('|')...
```

</panel>