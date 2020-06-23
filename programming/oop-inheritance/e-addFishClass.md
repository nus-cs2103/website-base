#### Exercise : Add `Fish` Class

Add a `Fish` class that inherits from the `Animal` class so that the code below produces the given output.

<include src="inputOutput.md" boilerplate> 
<span id="input">

```python
class Animal:
  def __init__(self, name):
    self.name = name
    
  def info(self):
    print("I'm a", self.name)
    
# ADD YOUR CODE HERE
    
tuna = Fish('Tuna')
tuna.info()
tuna.move()
guppy = Fish('Guppy')
guppy.info()
guppy.move()
```
</span>
<span id="output">

```{.no-line-numbers}
I'm a Tuna
I'm swimming
I'm a Guppy
I'm swimming
```
</span>
</include>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
class Fish(Animal):
  def move(self):
    ...
```

</panel>