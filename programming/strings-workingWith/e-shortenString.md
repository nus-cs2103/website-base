#### Exercise : Shorten String

Complete the function given below, to behave as described by its docstring.

```python
def shorten(text):
  """ Return a 10-character version of the string if it is longer.
  
  If text is longer than 10 characters, return the first four characters 
  followed by '..' followed by the last four characters.
  If text is not longer than 10 characters, return text.
  
  Example:
  shorten('1234567890abcd') returns '1234..abcd'
  """
  pass # REPLACE WITH YOUR CODE

```

Example usage:
<table> 
<tr>
  <td>

```python
print(shorten('1234'))    
print(shorten('1234567890'))
print(shorten('1234567890abcd'))
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
1234
1234567890
1234..abcd
```
  </td>
</tr>
</table>


<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
  if len(text) > 10:
    return text[:4] + '..' # ...
  else:
    return text
```

</panel>