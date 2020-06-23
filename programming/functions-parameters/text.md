### Function Parameters

**You can configure a function to have _parameters_. The code inside the function can use the parameters like variables.** That means we can pass arguments (i.e., values for those parameters) to affect the behavior of a function so that the function behaves differently each time it is executed.

Format:
```python
def function_name(parameter1_name, parameter2_name, ...):
    ...
```

****Parameters vs arguments:**** When you define a function, you can specify _parameters_ that it can accept. When you call the function, you can assign _arguments_ (i.e. values) to each of those parameters.

<tip-box> 

{{ icon_example }} The `say_hello` function below takes one parameter. The first time we call it we pass the argument `Gina` to that parameter, and the next time we pass a different argument `John` to the same parameter.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
def say_hello(name):
  print('Hello ' + name)
  print('How are you', name, '?')

say_hello('Gina')
say_hello('John')
```
</span>
<span id="output">

```
Hello Gina
How are you Gina ?
Hello John
How are you John ?

```
<include src="visualize.md" boilerplate >
  <span id="code">def%20say_hello%28name%29%3A%0A%20%20print%28'Hello%20'%20%2B%20name%29%0A%20%20print%28'How%20are%20you',%20name,%20'%3F'%29%0A%20%20%0Asay_hello%28'Gina'%29%0Asay_hello%28'John'%29</span>
</include>
</span>
</include>

<panel type="seamless" header="%%{{ icon_try }} Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/hello-name?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

{{ icon_example }} The code below has a `say_hello` function that takes one parameter and a `repeat_hello` function that takes two parameters. Furthermore, note how one function calls the other.

```python
def say_hello(name):
  print('Knock knock ' + name)

def repeat_hello(name, times):
  print('Greeting ', name, times, 'times')
  for i in range(times):
    say_hello(name)
  
repeat_hello('Penny', 3)
say_hello('Sheldon')
```
<include src="tryYourOwn.md" boilerplate var-program="hello-given-times" />

<panel type="seamless" header="%%:laughing: See the human version of the above code%%" minimized>
<iframe width="560" height="315" src="https://www.youtube.com/embed/jrzUsHNGZHc?rel=0&showinfo=0&start=0&end=15&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

</tip-box>

**Parameter values are forgotten after the function returns**.

<tip-box> 

{{ icon_example }} The code below produces an error because variable `v1` is not available after the function has returned.

```python
def print_uniqueness(v1, v2, v3):
  print(v1 != v2 and v2 != v3 and v3 != v1)
  
print_uniqueness(1,2,4) # True
print_uniqueness(1,1,2) # False

# Error. v1 is not available after function returns
print(v1) 
```

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Function parameters%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/WB4hJJkfhLU?rel=0&showinfo=0&start=199&end=315&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Grader `print_score` function" var-file="e-grader-printScoreFunction.md" />