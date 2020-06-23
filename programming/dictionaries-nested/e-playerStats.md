#### Exercise: Player Stats

Assume in each inning a player gets to bat a number of times and each hit can score 0, 1, 4, or 6, which are known as _hit sizes_. There is a need to keep track of how many times a player achieved each hit size in an inning.

Note how the `player_stats` dictionary in the code below uses lists which contain dictionaries to store, for each player, how many times the player scored a certain hit size, for each inning. For example, the player `amy` scored hit size of 0 x 0 times; hit size of 1 x 1 times; hit size of 4 x 1 times; hit size of 6 x 0 time in the first inning (which adds up to a score of `0*0 + 1*1 + 4*1 + 6*0 = 10` for her first inning).

```python
player_stats = {'amy': [{0:0, 1:1, 4:1, 6:0},  # amy's first inning stats
                        {0:2, 1:5, 4:0, 6:0},  # amy's second inning stats
                        {0:0, 1:0, 4:1, 6:1}], # amy's third inning stats
                'betty': [{0:2, 1:2, 4:2, 6:0}],
                'charlie': []}
```

Update the `get_player_hit_count(player_stats, player, inning, hit_size)` functions in the code such that it uses the `player_stats` dictionary to return the hit count for the `player` in the `inning` for the given `hit_size`.<br>
e.g., `get_player_hit_count(player_stats, 'amy', 2, 6)` should return how many times `amy`'s hits in her second inning (i.e., `inning = 2`) scored `6`s; the return value should be `0`.
```python
def get_player_hit_count(stats, player, inning, hit_size):
  return 0 #REPLACE WITH YOUR CODE!
  
print(get_player_hit_count(player_stats, 'amy', 2, 1))
print(get_player_hit_count(player_stats, 'betty', 1, 4))
```
{{ icon_output }}
```
5
2
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python

def get_player_hit_count(player_stats, player, inning, hit_size):
  return player_stats[...][inning-1][...]
```

</panel>