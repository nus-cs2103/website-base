#### Exercise : Add Class Level Members to `Subject` class

Add the following members to the `Subject` class in the code below so that the code produces the output given on the right.
* a class-level attribute `total` (type: `int`) that tracks the total number of `Subject` objects created
* a class-level method `limit_reached(limit)` that returns `True` (type: `bool`) if the `total` is greater than or equal to the specified `limit`.

<table>
<tr>
  <td>

```python
class Subject:
  
  def __init__(self, code, name):
    self.name = name
    self.code = code
    
  def print_info(self):
    print(self.code, ':', self.name)
    
print('total subjects:', Subject.total)
s1 = Subject('TE3201', 'Software Engineering') 
print('total subjects:', Subject.total)
print(Subject.limit_reached(1))
print(Subject.limit_reached(2))
s2 = Subject('TEE3201', 'Software Engineering')
print('total subjects:', Subject.total)
print(Subject.limit_reached(2))
print(Subject.limit_reached(3))
Subject.total = 100
print(Subject.limit_reached(100))
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom"> 

```
total subjects: 0
total subjects: 1
True
False
total subjects: 2
True
False
True
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution and hints%%">

```python
class Subject:
  
  # ADD `total` attribute here
  
  def __init__(self, code, name):
    self.name = name
    self.code = code
    Subject.total = Subject.total + 1 # Note this line
    
  def print_info(self):
    print(self.code, ':', self.name)
    
  @classmethod
  def limit_reached(cls, limit):
    ... # ADD implementation
```

</panel>