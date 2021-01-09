#### Exercise : Create Directory

Complete the functions given below, to behave as described by their docstrings, so that the code produces the given output. 

```python
import os

def create_dir(dir_name):
  """Create a directory dir_name in the current working directory
  
  Example:
  If the current directory is c:/foo/, create_dir('bar') creates 
  a c:/foo/bar directory.
  """
  pass # REPLACE WITH YOUR CODE HERE
  
  
def change_dir(relative_path):
  """Change to the directory dir_name relative to the current working directory
  
  Example:
  If the current directory is c:/foo/, change_dir('bar') changes 
  current working directory to c:/foo/bar
  """
  pass # REPLACE WITH YOUR CODE HERE
  
  
def print_current():
  """Print current working directory"""
  pass # REPLACE WITH YOUR CODE HERE 
  
  
def change_to_parent_dir():
  """Change to the parent directry of the current working directory
  
  Example:
  If the current directory is c:/foo/bar, change_to_parent_dir() changes 
  the working directory to c:/foo/
  """
  pass # REPLACE WITH YOUR CODE HERE
  
  
def check(dir_name):
  create_dir(dir_name)
  print_current()
  change_dir(dir_name)
  print_current()
  change_to_parent_dir()
  print_current()
  
check('foo')
check('bar')

```

{{ icon_output }} output when run in repl.it

```
/home/runner
/home/runner/foo
/home/runner
/home/runner
/home/runner/bar
/home/runner
```
  


<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
import os

def create_dir(dir_name):
  """Create a directory dir_name in the current working directory
  
  Example:
  If the current directory is c:/foo/, create_dir('bar') creates 
  a c:/foo/bar directory.
  """
  os.makedirs(dir_name)

...

def print_current():
  """Print current working directory"""
  print(os.getcwd())
```

</panel>