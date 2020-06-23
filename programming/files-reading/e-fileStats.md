#### Exercise : File Stats

Complete the functions given below, to behave as described by their docstrings, so that the code produces the given output.

```python
def get_file_content_as_list(filename):
  """Return content of the file as a list of lines
  
  The file is expected to be in the current working directory.
  The lines in the list contains trailing line breaks.
  
  Example:
  If the a.txt has two lines 'aaa' and 'bbb', 
  get_file_content_as_list('a.txt') returns ['aaa\n', 'bbb']
  """
  return [] # REPLACE WITH YOUR CODE


def get_file_stats(contents):
  """Given a list of lines, return line count and letter count as a dictionary
  
  Trailing line breaks (if any) are not counted for letter count.
  Spaces, even trailing spaces, are counted for letter count.
  Example:
  get_stats(['aaa\n', 'bbb']) returns {'lines': 2, 'letters': 6}
  """
  stats = []
  # ADD YOUR CODE HERE
  return stats


def analyze_file(filename):
  contents_as_list = get_file_content_as_list(filename)
  print('lines in file:', contents_as_list)
  stats = get_file_stats(contents_as_list)
  print('It has', stats[0], 'lines containing', stats[1], 'letters')

analyze_file('file1.txt')
analyze_file('file2.txt')
```

`file1.txt` (2 lines, 22 letters):
```
aaa bbb ccc
ddd eee fff
```

`file2.txt` (4 lines, 10 letters -- note: the ==last line has a trailing space==, which adds up to 10 letters):
```
a
bb
ccc
ddd 
```

{{ icon_output }}

```
lines in file: ['aaa bbb ccc\n', 'ddd eee fff']
It has 2 lines containing 22 letters
lines in file: ['a\n', 'bb\n', 'ccc\n', 'ddd ']
It has 4 lines containing 10 letters
```

<panel type="seamless" header="%%:bulb: Tips%%">

* `strip()` removes trailing line breaks but also trailing spaces. `replace('\n', '')` will remove the trailing line break but will keep the trailing spaces.

</panel>

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def get_file_content_as_list(filename):
  """Return content of the file as a list of lines
  
  The file is expected to be in the current working directory.
  The lines in the list contains trailing line breaks.
  
  Example:
  If the a.txt has two lines 'aaa' and 'bbb', 
  get_file_content_as_list('a.txt') returns ['aaa\n', 'bbb']
  """
  f = open(filename, 'r')
  lines = f.readlines()
  f.close()
  return lines
```

</panel>