### Variables

>**Variables are used to store information to be referenced and manipulated in a computer program.** They also provide a way of labeling data with a descriptive name, so our programs can be understood more clearly by the reader and ourselves. It is helpful to think of variables as containers that hold information. Their sole purpose is to label and store data in memory. This data can then be used throughout your program. <sub>--https://launchschool.com/books/ruby/read/variables (emphasis added)</sub>

The following statement _<tooltip content="creates">declares</tooltip>_ a variable named `v` and _assigns_ it a value `5` (the operator `=` is called the _assignment operator_):
```python
v = 5
``` 

<tip-box> 

**Statements**

Note that we called `v = 5` a _statement_. **Unlike expressions that evaluates to a single value, a statement does not evaluates to a value.** However, a statement can contain an expression e.g. `v = 5 + 8`.
</tip-box>

If you enter the above statement in the interactive shell, it causes the shell to remember the variable name `v` and its value. 
```python
>>> v = 5
>>> 
```
Now, you can ask the shell to recall the value by simply typing in the variable name as an expression.
```python
>>> v
5
```
You can even use the variable in expressions.
```python
>>> v * 4
20
```

<tip-box> 

{{ icon_example }} Here are some examples of variables being declared, assigned, and being used:

```python
>>> max_bag_count = 2
>>> max_bag_count
2

>>> price = 10.0
>>> discount_percentage = 5
>>> discount = price * discount_percentage / 100
>>> price - discount
9.5
```

<panel type="seamless" header="%%{{ icon_try }} Try your own%%">

<iframe src="https://trinket.io/embed/python/3d7b1ae52f?outputOnly=true&runOption=console&start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

</panel>
</tip-box>

**Python variable names (by convention) use lower case letters with `_` separating words.**
```python
long_variable_name = 56
```

**Variable names are case sensitive.** In the example below, you can see how Python prints an error message if you try to access the variable `height` using the name `Height`
```python
>>> height = 12.0

>>> height
12.0

>>> Height
Traceback (most recent call last):
 File "< pyshell#5 >", line 1, in < module >
   Height
NameError: name 'Height' is not defined
``` 

**Variables can be overwritten**. In the example below, `height` was initially `5` but the value is reassigned later to be `1` more than the previous value.

```python
>>> height = 5
>>> height
5

>>> height = height + 1
>>> height
6
```

**The value of one variable can be assigned to another variable.**

<tip-box>

{{ icon_example }} In the example below, the value of variable `height` is assigned to the variable `width`.
```python
>>> height = 5
>>> width = height
>>> width
5

>>> height + width
10

>>> height = 10
>>> width
5
```

<panel type="seamless" header="%%{{ icon_try }} Try your own%%">

<iframe src="https://trinket.io/embed/python/900dbf4e77?outputOnly=true&runOption=console&start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

</panel>
</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Variables%%">

<iframe width="560" height="315" src="https://www.youtube.com/embed/7qHMXu99d88?rel=0&start=417&end=614&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Circle Circumference" var-file="e-circle.md" />