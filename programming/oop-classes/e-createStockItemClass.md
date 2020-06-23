#### Exercise : Create `StockItem` Class

Define the `StockItem` class missing in the code below so that the code produces the output given on the right.

<table>
<tr>
  <td>

```python
# ADD StockItem class here
# It should have an attribute: name
# It should have a method: info() 
    
a = StockItem('Apple')
print(a.info())
print(a.name)
b = StockItem('Bag of Beans')
print(b.info())
b.name = 'Bananas'
print(b.info())
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom"> 

```
Item info: Apple
Apple
Item info: Bag of Beans
Item info: Bananas
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
class StockItem:
  
  def __init__(self, name):
    self.name = ...
    
  def info(self):
    return ...
```

</panel>