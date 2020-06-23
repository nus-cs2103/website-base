#### Exercise : Escape Sequences

Modify the `get_string()` function so that the code prints the given output.<br>
Note that these words are separated by tabs, not normal spaces:`"oops"`%%{tab here}%%`"ok"`%%{tab here}%%`"oh?"`
```python
def get_string():
  return '' # REPLACE WITH YOUR CODE

print(get_string())
```
{{ icon_output }}
```
Which word didn't he/she say? ["oops" "ok" "oh?"]
```

<panel type="seamless" header="%%:bulb: Tips%%">

* Use `\t` to print a tab character. 
* Use `\'` to print a single quote inside a string.

</panel>
<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def get_string():
  return 'Which word didn\'t he/she say? ...'

print(get_string())
```

</panel>