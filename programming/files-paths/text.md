### File Paths

A file has a _filename_ and a _path_. **The _path_ specifies the location of a file on the computer**, as a hierarchy of _folders_ (also called _directories_).

<box>

<tabs>
  <tab header="Windows">

{{ icon_example }} File `C:\photos\2018\home.jpg`

* Filename: `home.jpg`
* Path: `C:\photos\2018` (Windows uses the back slash `\` as the _separator_ symbol in paths )
* Folders in the path (`C:` is called the _root folder_):
  ```
  C: {root}
    └── photos
         └── 2018
  ```

{{ icon_important_big_red }} Windows file names and paths are not case sensitive: `C:\photos\2018\home.jpg` is same as `C:\PHOTOS\2018\HOME.JPG`.
  </tab>
  <tab header="OS-X/Linux">

{{ icon_example }} File `/Users/john/home.jpg`

* Filename: `home.jpg`
* Path: `/Users/john` (OS-X/Linux uses the forward slash `/` as the _separator_ symbol in paths )
* Folders in the path (the `/` at the start of the path is considered the _root folder_):
  ```
  / {root}
      └── Users
            └── john
  ```
{{ icon_important_big_red }} OS-X/Linux file names and paths are case sensitive. `/Users/john/home.jpg` is NOT the same as `/USERS/JOHN/HOME.JPG`

  </tab>
</tabs>

</box>

The Python module `os` contains functions for dealing with files and folders. For example, you can use `os.getcwd()` to get the <tooltip content="A program has a _working directory_ at any time; it can change over time">current working directory</tooltip> and `os.chdir()` to change the working directory to a different location.

<tip-box>

{{ icon_example }} This code shows how to print/change current working directory

```python
import os

cwd = os.getcwd() # store current working dir
print(cwd) # print current working dir
os.chdir('C:\\temp\\python') # change dir
print(os.getcwd()) # print current working dir
os.chdir(cwd) # change working dir back to original
print(os.getcwd())
```
{{ icon_output }}

```{.no-line-numbers}
C:\photos\vaction
C:\temp\python
C:\photos\vaction
```

{{ icon_tip }} Note how the path `'C:\\temp\\python'` uses double slash to <trigger trigger="click" for="modal:filePaths-stringsEscape">escape</trigger> the `\`. In OS-X or Linux, it can be something like `/user/john/python` (no need for double slash).

<modal large header="**Escape Sequences** %%(extrat from Strings → String Literals)%%" id="modal:filePaths-stringsEscape">
  <include src="../strings-literals\text.md#strings-escape"/>
</modal>

</tip-box>

**A path that specifies all folders starting from the root is an _absolute path_. A path that is specified relative to the current working directory is a _relative_ path.**

<box>

{{ icon_example }} Assume the current working directory is `C:\courses\tee3201` and you created a new folder inside it named `exercises` and put a `ex.txt` file in that folder.

* Absolute path of the file: `C:\courses\tee3201\exercises\ex1.txt`
* Relative path of the file: `exercises\ex1.txt`

</box>

In a path, you can use the  dot `.` as a shorthand to refer to the current working directory. Similarly, `..` can be used to refer to the parent directory.


<box>

{{ icon_example }} If the current working directory is `C:\courses\tee3201`, you can use any of the following to refer to `C:\courses\tee3201\exercises\ex1.txt`.
* `exercises\ex1.txt`
* `.\exercises\ex1.txt`
* `..\tee3201\exercises\ex1.txt`
* `..\..\courses\tee3201\exercises\ex1.txt`

<panel type="seamless" header="%%another example%%">

![](https://automatetheboringstuff.com/images/000032.jpg)
</panel>

</box>

You can use `os.makedirs()` function to create folders and `os.removedirs()` to delete folders.

<box>

{{ icon_example }} Example code showing how to create/delete directories

```python
print(os.getcwd())
os.makedirs('ex\\w1')
os.chdir('ex\\w1')
print(os.getcwd())
os.chdir('..') # go to parent dir
print(os.getcwd())
os.chdir('..')
os.removedirs('ex\\w1')
```
{{ icon_output }}
```{.no-line-numbers}
C:\repos\nus-tee3201\sample-code
C:\repos\nus-tee3201\sample-code\ex\w1
C:\repos\nus-tee3201\sample-code\ex
```

</box>

`os.path` module has many functions that can help with paths. For example, `os.paths.join()` function can be used to generate file path that matches the current operating system.

<box>

{{ icon_example }} Consider the code below:

```python
cwd = os.getcwd()
print(os.path.join(cwd, 'ex', 'w2'))
```

If you run it on a Windows computer in the folder `C:\courses\tee3201`, it prints `C:\courses\tee3201\ex\w2`.<br>
If your run it on a OS-X computer in the folder `/Users/john`, it prints `/Users/john/ex/w2`.

</box>

{{ icon_important_big_red }} To ensure that your code can work on any OS, you are advised to use `os.path.join()` function instead of hard-coding the <tooltip content="i.e., `\\` on Windows and `/` on OS-X/Linux">path separators</tooltip>.

<box>

{{ icon_example }} contrasting hard-coding the separator vs using `os.path.join()`:

* {{ bad }} (Works only on Windows):<br>
  `os.makedirs('ex\\w1')`
* {{ good }} (Works on both Windows and OS-X):<br>
  `os.makedirs(os.path.join('ex', 'w1'))`

</box>

<include src="exercisePanel.md" boilerplate var-title="Create Directory" var-file="e-createDir.md" />
