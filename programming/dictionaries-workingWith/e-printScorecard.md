#### Exercise: Print Scorecard

Update the functions in the code to behave as described below such that the code produces the output given below the code.

Given the parameter`scores` is a dictionary of the format `{'amy': 35, 'betty': 36, 'charlie': 30}` which contains scores of a bunch of players,
* `get_team_score(scores)`: returns the total of all scores of all players in `scores`.
* `print_scorecard(scores)`: prints scores of each player in the format given, in the alphabetical order of player names.


```python
def get_team_score(scores):
  total = 0
  #ADD YOUR CODE HERE!
  return total
  
def print_scorecard(scores):
  #pass #REPLACE WITH YOUR CODE!

game2_scores = {'zac': 35, 'betty': 30, 'aaron': 10}
print_scorecard(game2_scores)
print('total =', get_team_score(game2_scores))
```
{{ icon_output }}
```
aaron = 10
betty = 30
zac = 35
total = 75
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
for p in scores.keys():
  ...
  
for p in sorted(scores.keys()):
  ...
```

</panel>