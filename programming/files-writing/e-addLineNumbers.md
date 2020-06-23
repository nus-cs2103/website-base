#### Exercise : Add Line Numbers

Complete the functions given below, to behave as described by their docstrings, so that the code produces the given output. Only one function needs to be modified.

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
  
def write_with_line_numbers(lines, filename):
  """Write the strings in lines to the file filename, after adding a line number to each line.
  
  Example:
  write_with_line_numbers(['aaa\n', 'bbb'], 'out.txt') writes the following content to out.txt
  1. aaa
  2. bbb
  """
  pass # REPLACE WITH YOUR CODE


def process_file(sourcefile, targetfile):
  """Copy the text in sourcefile to targetfile, but also add line numbers to each line.
  
  Example:
  Assume a.txt has the following text:
  aaa
  bbb
  process_file('a.txt', 'b.txt') results in b.txt having the following text:
  1. aaa
  2. bbb
  """
  contents = get_file_content_as_list(sourcefile)
  write_with_line_numbers(contents, targetfile)
  print(get_file_content_as_list(targetfile))
  
process_file('file1a.txt', 'file1b.txt')
process_file('file2a.txt', 'file2b.txt')

```

`file1a.txt`:
```
first line

second line
third line
```

`file2a.txt`:
```
hang in there
```

{{ icon_output }}

```
['1. first line\n', '2. \n', '3. second line\n', '4. third line']
['1. hang in there']
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def write_with_line_numbers(lines, filename):
  """Write the strings in lines to the file filename, after adding a line number to each line.
  
  Example:
  write_with_line_numbers(['aaa\n', 'bbb'], 'out.txt') writes the following content to out.txt
  1. aaa
  2. bbb
  """
  for n,line in enumerate(lines):
    f.write(str(n+1) ... ) # COMPLETE THIS LINE
  f.close()

```

</panel>