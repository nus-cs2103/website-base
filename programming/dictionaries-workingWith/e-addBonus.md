#### Exercise: Add Bonus

Update the functions in the code to behave as described below such that the code produces the output given below the code.

Given the parameter`scores` is a dictionary of the format `{'amy': 35, 'betty': 36, 'charlie': 30}` which contains scores of a bunch of players,
* `add_bonus(scores, player, bonus)`: adds the `bonus` to the value of the `player` if player already exists in `scores`. Otherwise, adds the `player` to `scores` with the value `bonus`.


```python
def add_bonus(scores, player, bonus):
  pass #REPLACE WITH YOUR CODE!


game3_scores = {'amy': 35, 'betty': 36, 'charlie': 30}    
add_bonus(game3_scores, 'amy', 5)
add_bonus(game3_scores, 'dan', 10)
print(game3_scores)
```
{{ icon_output }}
```
{'amy': 40, 'betty': 36, 'charlie': 30, 'dan': 10}
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def add_bonus(scores, player, bonus):
  if player in scores.keys():
    ...
  else:
    ...
```

</panel>