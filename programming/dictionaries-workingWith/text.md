### Working with Dictionaries

**You can use keys to access values in a dictionary.**

<box>

{{ icon_example }} Some examples of retrieving values based on the key:

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
numbers = {1: 'one', 2: 'two', 3: 'three'}
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
print(type(numbers))
print(numbers[1])
print(prices['butter'])
```
</span>
<span id="output">

```
<class 'dict'>
one
5.0
```
</span>
</include>

{{ icon_example }} Examples of adding, updating, and deleting dictionary entries:

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
grades = {'TE3201': 'A'}
grades['CS2103'] = 'B'
print('After adding:',grades)
grades['TE3201'] = 'A+'
print('After updating:',grades)
del grades['CS2103']
print('After deleting:', grades)
```
</span>
<span id="output">

```
After adding: {'TE3201': 'A', 'CS2103': 'B'}
After updating: {'TE3201': 'A+', 'CS2103': 'B'}
After deleting: {'TE3201': 'A+'}
```
</span>
</include>

</box>

<include src="exercisePanel.md" boilerplate var-title="Get Set Delete Score" var-file="e-getSetDeleteScore.md" />

**Trying to access a value for a non-existent key raises a `KeyError` exception.**

<box>

{{ icon_example }} This example raises an exception because the key `'santa'` does not exist in the dictionary `is_nice`:

<include src="inputOutput.md" var-align="top" boilerplate>
<span id="input">

```python
is_nice = {'jane': False, 'hakim': True}
print(is_nice['santa'])
```
</span>
<span id="output">

```
Traceback (most recent call last):
  File "python", line 9, in <module>
KeyError: 'santa'
```
</span>
</include>

</box>

<include src="exercisePanel.md" boilerplate var-title="Get Score with Error Handling" var-file="e-getScoreWithErrorHandling.md" />

**You can use `keys()` and `values()` methods to iterate through keys and values of a dictionary, respectively.**

<box>

{{ icon_example }} The code below shows how to iterate through keys/values of a dictionary.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
for k in prices.keys():
  print(k, '->', prices[k])
```
</span>
<span id="output">

```
bread -> 3.5
butter -> 5.0
banana -> 0.15
```
</span>
</include>

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
for v in prices.values():
  print(v)
```
</span>
<span id="output">

```
3.5
5.0
0.15
```
</span>
</include>

</box>

You can **use the `sorted()` function to sort the keys/values before iterating through them**.

<box>

{{ icon_example }} The code below shows how to iterate through keys/values of a dictionary.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
for k in sorted(prices.keys()):
  print(k, '->', prices[k])
```
</span>
<span id="output">

```
banana -> 0.15
bread -> 3.5
butter -> 5.0
```
</span>
</include>

</box>

<include src="exercisePanel.md" boilerplate var-title="Print Scorecard" var-file="e-printScorecard.md" />

As usual, you can **use `in` and `not in` to check whether a key or a value is in a dictionary**.

<box>

{{ icon_example }} The code below shows how to check if a certain key or a value exists in a dictionary.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
print('bread' in prices.keys())
print('sugar' not in prices.keys())
```
</span>
<span id="output">

```
True
True
```
</span>
</include>

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
print(3.5 in prices.values())
print(6.0 in prices.values())
```
</span>
<span id="output">

```
True
False
```
</span>
</include>

</box>

<include src="tryYourOwn.md" boilerplate var-program="dictionaries-workingWith" />

<include src="exercisePanel.md" boilerplate var-title="Add Bonus" var-file="e-addBonus.md" />