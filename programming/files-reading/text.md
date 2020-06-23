### Reading from Files

This section focuses on reading from text-based files (i.e., not binary files).

**There are three steps to reading files in Python:**
* Call the **`open()`** function to receive a `File` object.
* Call the **`read()`** method on the `File` object to receive file content.
* Close the file by calling the **`close()`** method on the `File` object.

<tip-box> 

{{ icon_example }} The code below shows how to read from a text file.

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

```python
file_path = os.path.join('data', 'items.txt')
f = open(file_path, 'r') # open in read mode
items = f.read()
print(items)
f.close()
```
</span>
<span id="output">

Output (contents of the `items.txt`):
```
first line
second line
third line
```
</span>
</include>

{{ icon_tip }} The `'r'` argument in `open(file_path, 'r')` indicates that the file should be opened <tooltip content="when a file is open in read mode, you can read from it but cannot write to it">in read mode</tooltip>.

</tip-box>

It is also possible to read the file content as a list of lines, using the `readlines()` method.

<tip-box> 

{{ icon_example }} The code below shows how to read file content as a list of lines.

```python
file_path = os.path.join('data', 'items.txt')
f = open(file_path, 'r')
items = f.readlines()
print(items) # print as a list
for i in items: # print each item
  print(i.strip()) # use strip() to remove linebreak at the end of each line
f.close()
```
{{ icon_output }}
```
['first line\n', 'second line\n', 'third line\n']
first line
second line
third line
```
{{ icon_tip }} Note how each line ends with a `\n` which represents the line break. It can be removed using the `strip()` method.

</tip-box>

<include src="exercisePanel.md" boilerplate var-title="File Stats" var-file="e-fileStats.md" />