#### Exercise : Rectify Case

Complete the `rectify_case(text)` function given below, to behave as follows:
* If `text` is all upper case, return `text` in lower case
* If `text` is all lower case, return `text` in upper case
* Return `text` otherwise

```python
def rectify_case(text):
  #pass # REPLACE WITH YOUR CODE

```

Example usage:
<include src="inputOutput.md" boilerplate>
<span id="input">

```python
print(rectify_case('Mrs. Fox'))
print(rectify_case('MR. FOX'))
print(rectify_case('baby fox'))
```
</span>
<span id="output">

```
Mrs. Fox
mr. fox
BABY FOX
```
</span>
</include>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
  if text.isupper(): 
    return text.lower()
  ...
```

</panel>