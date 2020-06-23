#### Exercise : Print Card Deck

Complete the functions as described below:
* `print_card_deck()`: Prints all cards in a deck of regular playing cards, en example of the output (partial) is given below.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def print_card_deck():
  suits = ['♣', '♦', '♥', '♠']
  ranks = ['A', '2', '3', '4', '5', '6', '7', '8', '9', '10', 'J', 'Q', 'K']

print_card_deck()

```
</span>
<span id="output">

```
A of ♣
2 of ♣
3 of ♣
4 of ♣
5 of ♣
6 of ♣
...
```
</span>
</include>


<panel type="seamless" header="%%:bulb: Hint%%">

Use two nested `for` loops to iterate over the two lists.

</panel>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
  ...
  for suite in suits:
    for ...:
      print(...)
```
</panel>