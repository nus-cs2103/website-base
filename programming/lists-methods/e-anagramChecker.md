#### Exercise : Anagram Checker

Complete the functions as described below:
* `is_anagram(word1, word2)`: returns `True` if `word1` is an anagram of `word2`(i.e., letters of `word1` can be rearranged to get `word2` e.g., `ton` and `not` are anagrams).

You may find these built-in functions useful to this exercise:
* `list(string)`: splits a string into a list of letters.<br>
  e.g., `list('quick')` → `['q', 'u', 'i', 'c', 'k']`

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def is_anagram(word1, word2):
  return  # REPLACE WITH YOUR CODE

print(is_anagram('santa', 'damith'))
print(is_anagram('santa', 'satan'))
```
</span>
<span id="output">

```
False
True
```
</span>
</include>


<panel type="seamless" header="%%:bulb: Hint%%">

Convert each word into a list of letters and sort the letters. If the words are anagrams, sorted letters of one word should be same as the sorted letters of the others.

Example:
* `'ton'` → convert to list of letters → `['t', 'o', 'n']` → sort → `['n', 'o', 't']`
* `'not'` → convert to list of letters → `['n', 'o', 't']` → sort → `['n', 'o', 't']`

</panel>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def letters_sorted(word):
  letters = list(word)
  letters.sort()
  return letters
  
def is_anagram(word1, word2):
  return letters_sorted(word1) == ...
```

</panel>