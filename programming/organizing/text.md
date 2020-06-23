## Appendix C: Organizing Python Code

**You can organize the code as multiple files.** Python considers each file as a _module_. To use a function/class in one file from another, you need to `import` it first.

<box>

{{ icon_example }} Consider the following two files residing in the same directory.

`[project_root]/student.py`:
```python
def describe(name):
    print(name, 'is a student')
```

`[project_root]/course.py`:
```python
import student

student.describe('Adam')
```

Notice how the `course.py` imports the `student` module and uses the `student.describe` function defined in the `student.py` file.

</box>

**You can organize files into sub-directories too.**

<box>

{{ icon_example }} Consider the following two files.

`[project_root]/misc/print_utils/misc.py`:
```python
def print_as_list(text):
    print(list(text))
```

`[project_root]/course.py`:
```python
from utils.print_utils import misc 

misc.print_as_list('Adam')
```

Notice how the `import` statement uses a slightly different syntax and uses `.` to indicate directory nesting (i.e., `misc/print_utils` → `misc.print_utils`). In fact, there are [other variations of the `import` syntax](https://docs.python.org/3/tutorial/modules.html).

</box>

When you import a module, Python will interpret and execute any code in it. 

<box>

{{ icon_example }} Consider this `student` module being imported into the `course` module. 

`[project_root]/student.py`:
```python
def describe(name):
    print(name, 'is a student')

describe('Betty')
```

<include src="inputOutput.md" boilerplate> 
<span id="input">

`[project_root]/course.py`:
```python
import student

student.describe('Adam')
```
</span>
<span id="output">

```{.no-line-numbers}
Betty is a student
Adam is a student
```
</span>
</include>

Notice how the output contains `Betty is a student`. That is because the line `describe('Betty')` in `student.py` is being executed as the `student` module is being imported.

</box>

To prevent execution of statements in an imported module, nest such statements under a `if __name__ == "__main__":`{.python} block.

<box>

{{ icon_example }} In the code below, the `student` module can be executed to get the following output.

<include src="inputOutput.md" boilerplate> 
<span id="input">

`[project_root]/student.py`:
```python
def describe(name):
    print(name, 'is a student')

if __name__ == "__main__":
    describe('Betty')
```
</span>
<span id="output">

```{.no-line-numbers}
Betty is a student
```
</span>
</include>

When the `student` module is imported to another module, `describe('Betty')` line is no longer executed.

<include src="inputOutput.md" boilerplate> 
<span id="input">

`[project_root]/course.py`:
```python
import student

student.describe('Adam')
```
</span>
<span id="output">

```{.no-line-numbers}
Adam is a student
```
</span>
</include>

</box>