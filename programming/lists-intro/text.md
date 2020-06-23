### The List Data Structure

**A _data structure_ contains data that are more complex than a single data value** such as an integer. Lists are one such very useful data structure used in Python. **A list contains an ordered sequence of _items_.** Python uses square brackets to indicate lists.

<tip-box> 

{{ icon_example }} Some list examples:
  
```python
friends = [] # an empty list
fruits = ['apple', 'banana', 'orange'] # a list containing 3 string items
values = [0, 3.4, 'High', True] # a list containing items of different types
print(friends, fruits, values)

everything = [friends, fruits, values] # a list containing other lists
print(everything)
```
{{ icon_output }}
```
[] ['apple', 'banana', 'orange'] [0, 3.4, 'High', True]
[[], ['apple', 'banana', 'orange'], [0, 3.4, 'High', True]]
```
</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Lists%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=11&end=70&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Countries" var-file="e-countries.md" />

**You can use the notation `list_name[index_of_item]` to access an item of a list.** List indexes start from `0` i.e., the first item in a list has the index `0`.

<tip-box>

{{ icon_example }} The code below shows how to use indexes to access items in a list.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
fruits = ['Apple', 'Banana', 'Cherry', 'Dragon fruit']
print(fruits[0])
print(fruits[3])
print(fruits[-1])
print(fruits[-2])
```
</span>
<span id="output">

```
Apple
Dragon Fruit
Dragon Fruit
Cherry
```
</span>
</include>

{{ icon_tip }} As you can see from the above example, **list indexes can be negative**; index `-1` refers to the last item in the list, `-2` refers to the second last item in the list, and so on.

{{ icon_example }} The code below shows how to use indexes to update items in a list.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
coins = [10, 30, 50, 100]
coins[1] = 20
print(coins)
```
</span>
<span id="output">

```
[10, 20, 50, 100]
```
</span>
</include>


{{ icon_example }} The example below shows how to access an item of a list that is inside another list; `list_of_lists[2]` accesses `list_of_lists[2]` which gives you the item at index 2 (`[0.1, 0.2]`) which is also a list, and then accesses the item at index `0` from that list, which is `0.1`.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
list_of_lists = [['a', 'b', 'c'], [1, 2, 3, 4], [0.1, 0.2]]
print(list_of_lists[2][0])
```
</span>
<span id="output">

```
0.1
```
</span>
</include>

<include src="tryYourOwn.md" boilerplate >
  <span id="program">lists-access-using-index</span>
</include>

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Accessing an item from a list%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=70&end=317&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Get Head, Get Tail" var-file="e-getHeadTail.md" />
