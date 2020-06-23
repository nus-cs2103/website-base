#### Exercise : Add `SmartPhone` Class

Add a `SmartPhone` class to inherits from the `Camera` class and the `Phone` class so that the code below produces the given output.

<include src="inputOutput.md" boilerplate> 
<span id="input">

```python
class Camera:
  
  def take_photo(self):
    print('taking photo')
    
class Phone:
  
  def make_call(self):
    print('making call')
    
# ADD SmartPhone CLASS HERE

iphone = SmartPhone('iPhone')
iphone.take_photo()
iphone.make_call()
iphone.play_game()
```
</span>
<span id="output">

```{.no-line-numbers}
My model: iPhone
taking photo
making call
playing game
```
</span>
</include>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
class SmartPhone(Camera, Phone):
  
  def __init__(self, name):
    ...
  
  def play_game(self):
    ...
```

</panel>