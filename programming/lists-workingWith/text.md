### Working with Lists

**You can use `del` to delete an item at a specific position of a list.**

<tip-box>

{{ icon_example }} The code below shows how to use `del` to delete items in a list.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
spam = ['foo', 45.0, True]
del spam[-1] # delete last item
print(spam)
```
</span>
<span id="output">

```
['foo', 45.0]
```
</span>
</include>

<include src="tryYourOwn.md" boilerplate var-program="lists-del" />

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Deleting items from a list%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=534&end=581&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Delete Head, Delete Tail" var-file="e-deleteHead.md" />


**You can use the _slice_ notation `list_name[start_index:end_index]` to copy a _<tooltip content="a portion of a list">sublist</tooltip>_ into a new list.** If the `start_index` is omitted, it means 'from the beginning of the list'. If the `end_index` is omitted, it means 'till the end of the list'.

<tip-box> 

{{ icon_example }} Some example of slicing to get a sub list:

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
letters = ['0a', '1b', '2c', '3d', '4e']
sublist = letters[0:3]
print(sublist) # print items 0, 1, 2
print(letters[:3]) # same as above (first 3 items)
print(letters[1:4]) # print items 1, 2, 3
print(letters[3:]) # print from item 3 till end
print(letters[-2:]) # print last two items
print(letters[1:-1]) # print from item 1 to 2nd last item
```
</span>
<span id="output">

```
['0a', '1b', '2c']
['0a', '1b', '2c']
['1b', '2c', '3d']
['3d', '4e']
['3d', '4e']
['1b', '2c', '3d']
```
</span>
</include>

<include src="tryYourOwn.md" boilerplate var-program="lists-slicing" />

</tip-box>

Note that slicing gives you a _copy_ of a portion of the original list i.e., you get a new list.

<box>

{{ icon_example }} In the example below, the first item `0a` of the list `letters` is deleted after taking the first two elements as a sub list. Note how the item `0a` still remains in the sub list after it has been deleted from the original list.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
letters = ['0a', '1b', '2c', '3d', '4e']
first_two_letters = letters[:2]
print('original list:', letters)
print('sub list     :', first_two_letters)
del letters[0] # delete first element in original list
print('original list:', letters)
print('sub list     :', first_two_letters)
```
</span>
<span id="output">

```
original list: ['0a', '1b', '2c', '3d', '4e']
sub list     : ['0a', '1b']
original list: ['1b', '2c', '3d', '4e']
sub list     : ['0a', '1b']
```
</span>
</include>

<include src="tryYourOwn.md" boilerplate var-program="lists-slicing" />

</box>


<panel type="seamless" header="%%{{ icon_video }} Accessing multiple items from a list%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=317&end=534&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Get Body" var-file="e-getBody.md" />


**You can use the `len` function to find the number of items in a list.**

<tip-box> 

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
spam = ['a','b']
print('Length is:', len(spam))
```
</span>
<span id="output">

```
Length is: 2
```
</span>
</include>

<include src="tryYourOwn.md" boilerplate var-program="lists-len-plus-star-for" />

</tip-box>

<include src="exercisePanel.md" boilerplate var-title="Get Mid" var-file="e-getMid.md" />

**You can use the `+` operator to combine multiple lists into a new list.**

<tip-box> 

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
girls = ['Amy', 'Betsy', 'Clara']
boys = ['Adam', 'Ben']
friends = girls + boys
print(friends)
```
</span>
<span id="output">

```
['Amy', 'Betsy', 'Clara', 'Adam', 'Ben']
```
</span>
</include>

<include src="tryYourOwn.md" boilerplate var-program="lists-len-plus-star-for" />

</tip-box>

**You can use the `*` operator to create a new list by replicating an existing list multiple times.**

<tip-box> 

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
steps = ['left', 'right']
walking = steps*3
print(walking)
```
</span>
<span id="output">

```
['left', 'right', 'left', 'right', 'left', 'right']
```
</span>
</include>


<include src="tryYourOwn.md" boilerplate var-program="lists-len-plus-star-for" />

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Length of a list, list concatenation, list replication%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=581&end=635&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Expand to Fill" var-file="e-expandToFill.md" />

**You can use `in` or `not in` to check if an item is in a list**. 

<tip-box> 

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
valid_responses = ['Yes', 'No', 'Maybe']
response = ''
while response not in valid_responses:
  response = input('What is your response?')
print('Your response:', response)

current_drinks = ['Tea', 'Coffee']
suggested_drink = input('Suggest a new drink:')
if suggested_drink in current_drinks:
  print(suggested_drink, 'is already in the list')
```
</span>
<span id="output">

```
What is your response? abc
What is your response? Yes
Your response: Yes
Suggest a new drink: Tea
Tea is already in the list
```
</span>
</include>

<include src="tryYourOwn.md" boilerplate var-program="lists-in-not-in" />

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Checking if an item is in a list%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=675&end=742&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="XOR" var-file="e-xor.md" />

**You can traverse through items in a list using the `for item_name in list_name:` notation**.

<tip-box> 

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
pets = ['Cats', 'Dogs', 'Hamsters']
for animal in pets:
  print('Do you sell '+ animal +'?')
```
</span>
<span id="output">

```
Do you sell Cats?
Do you sell Dogs?
Do you sell Hamsters?
```
</span>
</include>

<include src="tryYourOwn.md" boilerplate var-program="lists-len-plus-star-for" />

</tip-box>

<include src="exercisePanel.md" boilerplate var-title="Print Card Deck" var-file="e-printCardDeck.md" />

**The `enumerate` function can help you easily maintain an iteration counter while traversing a list**.

<tip-box> 

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
pets = ['Cats', 'Dogs', 'Hamsters']
for i, animal in enumerate(pets):
  print(i+1, 'Can I buy '+ animal +'?')
```
</span>
<span id="output">

```
1 Can I buy Cats?
2 Can I buy Dogs?
3 Can I buy Hamsters?
```
</span>
</include>


<include src="tryYourOwn.md" boilerplate var-program="lists-len-plus-star-for" />

</tip-box>

<include src="exercisePanel.md" boilerplate var-title="First Quarter" var-file="e-firstQuarter.md" />