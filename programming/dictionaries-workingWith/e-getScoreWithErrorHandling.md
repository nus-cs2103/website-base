#### Exercise: Get Score with Error Handling

Update the `get_score1(scores, player)` function to handle error situations, as described below.

Given the parameter`scores` is a dictionary of the format `{'amy': 35, 'betty': 36, 'charlie': 30}` which contains scores of a bunch of players,
* `get_score1(scores, player)`: returns the value of the key `player`. ==Returns an error message if the `player` is not in `scores`==.


```python
def get_score1(scores, player):
  return scores[player] # UPDATE HERE!
    
game1_scores = {'amy': 35, 'betty': 36, 'charlie': 30}
print(get_score1(game1_scores, 'charlie'))
print(get_score1(game1_scores, 'brown'))
```
{{ icon_output }}
```
30
brown is not in the game!
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def get_score1(scores, player):
  try:
    return scores[player]
  except KeyError:
    ...
```

</panel>