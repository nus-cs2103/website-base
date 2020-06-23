#### Exercise: Inning-Scores

Assume the game has three innings and a player can play in 0-3 innings. For each inning, a player will have a inning-score which is an integer %%e.g., player `amy` scored `5`, `5`, and `10` for the three innings (in order)%%.

Update the `get_detailed_scores` functions in the code below such that it returns a dictionary that stores inning scores of each player as a ==list of integers for each player==. Inning-scores of each player is given below.

Player | Scores in different innings
-------|---------------------------
amy    | 5, 5, 10
betty  | 10
charile| (did not play any innings)

```python
def get_detailed_scores():
  return {'amy': 20, 'betty': 30, 'charlie': 30} #REPLACE WITH YOUR CODE! 

print(get_detailed_scores())
```
{{ icon_output }}
```
{'amy': [5, 5, 10], 'betty': [10], 'charlie': []}
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def get_detailed_scores():
  return {'amy': [5, 5, 10],
          ...}
```

</panel>