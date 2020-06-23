#### Exercise : Is Doctor

Complete the `is_doctor(name)` function to return `True` for the following cases:
* If `name` has a `Dr.` at the start
* If `name` has a `(Dr)` at the end

Note that the matching should be ==case-insensitive==.

```python
def is_doctor(name):
  #pass # REPLACE WITH YOUR CODE
```

Example usage:
<include src="inputOutput.md" boilerplate>
<span id="input">

```python
print(is_doctor('Dr. Jekyll'))
print(is_doctor('DR. Jekyll'))
print(is_doctor('dR. Jekyll'))
print(is_doctor('dr. Jekyll'))
print(is_doctor('Jekyll (Dr)'))
print(is_doctor('Jekyll (DR)'))
print(is_doctor('Jekyll (dr)'))
print(is_doctor('Mr. Hyde'))
print(is_doctor('Miss Dr. B.more'))
```
</span>
<span id="output">

```
True
True
True
True
True
True
True
False
False
```
</span>
</include>

<panel type="seamless" header="%%:bulb: Tips%%">

Convert the `name` to lower case and match with `dr.` or `(dr)` using string methods `startswith()`/`endswith()`

</panel>
<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
  name = name.lower()
  return name.startswith('dr.') ...
```

</panel>