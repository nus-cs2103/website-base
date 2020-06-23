#### Exercise : Change Visibility of `School` Class Members

Change the visibility of the members of the `School` class from private to public in the code below so that the code produces the output given on the right.

<table>
<tr>
  <td>

```python
class School:
  
  __target = 0.99
  
  def __init__(self, capital):
    self.__budget = capital
    
  def __max_expenditure(self):
    return self.__budget * School.__target
    
print(School.__target)
s = School(100000)
print(s.__budget)
print(s.__max_expenditure())
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom"> 

```{.no-line-numbers}
0.99
100000
99000.0
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:bulb: Hint%%">

Remove the leading underscores of the member names e.g., `__target` → `target`

</panel>