### Writing Functions

**You can write your own functions in Python.** Function are useful when you want to execute a bunch of statements multiple times at different points of a program. 

Format:
```python
def function_name():
    statement_1
    statement_2
    ...
```

<tip-box> 

{{ icon_example }} The code below defines a function named `say_hello` and calls it twice.

<include src="inputOutput.md" boilerplate >
<span id="input">

```python
def say_hello():
  print('Hello!')
  print('How are you?')
  print('Nice to meet you.')

# call the function twice
print('Going to call the function ...')
say_hello()
print('Going to repeat ...')
say_hello()
```
</span>
<span id="output">

```
Going to call the function ...
Hello!
How are you?
Nice to meet you.
Going to repeat ...
Hello!
How are you?
Nice to meet you.

```

<include src="visualize.md" boilerplate >
  <span id="code">def%20say_hello%28%29%3A%0A%20%20print%28'Hello!'%29%0A%20%20print%28'How%20are%20you%3F'%29%0A%20%20print%28'Nice%20to%20meet%20you.'%29%0A%20%20%0A%23%20call%20the%20function%20twice%0Aprint%28'Going%20to%20call%20the%20function%20...'%29%0Asay_hello%28%29%0Aprint%28'Going%20to%20repeat%20...'%29%0Asay_hello%28%29</span>
</include>

</span>
</include>

Note how the statements inside the function are not executed unless the method is called.

<include src="tryYourOwn.md" boilerplate var-program="hello-function" />

</tip-box>

The function definition should appear in the code _before_ it is called.
 
<tip-box> 

<table>
<tr>
  <td>

{{ good }} (this works)
```python
print('starting ...')

def say_hello():
  print('Hello!')

print('Going to say hello ...')

say_hello()
```
  </td>
  <td>&nbsp;&nbsp;</td>
  <td>
  
{{ bad }} (this will not work!)
```python
print('starting ...')
print('Going to say hello ...')

# call appears before definition
say_hello()

def say_hello():
  print('Hello!')
```
  </td>
</tr>
</table>

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Defining your own functions%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/WB4hJJkfhLU?rel=0&showinfo=0&start=13&end=199&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Hip Hip Hooray!" var-file="e-hooray.md" />