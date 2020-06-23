#### Exercise: Get, Set, Delete Score

Complete the three function below such that the code produces the given output.

Given the parameter`scores` is a dictionary of the format `{'amy': 35, 'betty': 36, 'charlie': 30}` which contains scores of a bunch of players,
* `get_score(scores, player)`: returns the value of the key `player`
* `set_score(scores, player, new_score)`: sets the value of the key `player` to the `new_score`
* `delete_score(scores, player)`: deletes the value for key `player`

```python
def get_score(scores, player):
  return # UPDATE HERE!
    
def set_score(scores, player, new_score):
  pass # REPLACE THIS WITH YOUR CODE!
  
def delete_score(scores, player):
  pass # REPLACE THIS WITH YOUR CODE!
  
game1_scores = {'amy': 35, 'betty': 36, 'charlie': 30}
print(get_score(game1_scores, 'betty'))
print(get_score(game1_scores, 'amy'))
set_score(game1_scores, 'charlie', 5)
set_score(game1_scores, 'dan', 0)
print(game1_scores)
delete_score(game1_scores, 'dan')
print(game1_scores)
```
{{ icon_output }}
```
36
35
{'amy': 35, 'betty': 36, 'charlie': 5, 'dan': 0}
{'amy': 35, 'betty': 36, 'charlie': 5}
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def get_score(scores, player):
  return scores[player]
    
def set_score(scores, player, new_score):
  scores[player] = new_score
```

</panel>