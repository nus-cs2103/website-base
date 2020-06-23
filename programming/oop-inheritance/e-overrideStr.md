#### Exercise : Override `__str__()` Method

Override the `__str()__` of the `Person` class so that the code below produces the given output.

<include src="inputOutput.md" boilerplate> 
<span id="input">

```python
class Person:
  
  def __init__(self, name, age):
    self.name = name
    self.age = age
  
  # OVERRIDE __str__ METHOD HERE
    
print(Person('Amy', 25))
print(Person('Ben', 26))
```
</span>
<span id="output">

```{.no-line-numbers}
Amy (25years)
Ben (26years)
```
</span>
</include>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def __str__(self):
    return self.name + ...
```

</panel>