### `while` Statements

**Python uses the `while` statement to repeat a code block until a certain condition is true. Such an execution path is also known as a _loop_ and each execution of the code block is called an _iteration_.**

Format:
```
while condition :
    statements_to_execute_if_condition_is_true
```
<tip-box>

{{ icon_example }} the code below prints 'Hello' 3 times (i.e., the loop is executed for 3 iterations), followed by 'Done'.

<table>
<tr>
  <td>

```python
counter = 0
while counter < 3:
    print('Hello')
    counter = counter + 1
print('Done')
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```
Hello
Hello
Hello
Done
```
<include src="visualize.md" boilerplate >
  <span id="code">counter%20%3D%200%0Awhile%20counter%20%3C%203%3A%0A%20%20%20%20print%28'Hello'%29%0A%20%20%20%20counter%20%3D%20counter%20%2B%201%0Aprint%28'Done'%29</span>
</include>

  </td>
</tr>
</table>


<panel type="seamless" header="%%{{ icon_try }} Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/hello-thrice?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Basic `while` loops%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/885qKiiKisI?rel=0&showinfo=0&start=8&end=107&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<tip-box>

**{{ icon_important_big_red }} Infinite Loops**: Sometimes programming mistakes can result in _infinite loops_ %%&nbsp;i.e., loops that never terminate.%% In the example below, the condition `counter < 3` always evaluates to `True` (because the statement to increment `counter` has been left out by mistake)

```python
counter = 0
while counter < 3:
    print('Hello')
```

{{ icon_tip }} When using IDLE, if a bug in your code caused it to go into an infinite loop,  you can use `Ctrl + C` to force it to stop executing.

<panel type="seamless" header="%%{{ icon_video }} Infinite loops%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/885qKiiKisI?rel=0&showinfo=0&start=297&end=340&version=3" frameborder="0" allowfullscreen></iframe>

</panel>

</tip-box>

<include src="exercisePanel.md" boilerplate var-title="Vending Machine - Add Loop" var-file="e-vending-oneCoin.md" />
<include src="exercisePanel.md" boilerplate var-title="Vending Machine - Accept Multiple Coins" var-file="e-vending-multipleCoins.md" />  

**You can use a `break` statement to break out of a loop.**

<tip-box> 

{{ icon_example }} The code below uses the `break` statement to break out of the loop when the password given is `abcd`. Without the `break` statement, the loop will repeat forever because the condition in `while True:` is always `True`.

```python
while True:
  password = input('What is the password?')
  if password == 'abcd':
    break # exit the loop
  else:
    print('Password incorrect. Try again.')
print('Password correct. You may proceed.')
```

<panel type="seamless" header="%%{{ icon_try }} Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/password-loop?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} `break` inside `while` loops%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/885qKiiKisI?rel=0&showinfo=0&start=346&end=409&version=3" frameborder="0" allowfullscreen></iframe>

</panel>

<include src="exercisePanel.md" boilerplate var-title="Vending Machine - Allow Abort" var-file="e-vending-allowAbort.md" /> 

**You can use a `continue` statement to skip the remainder of the current iteration** and go back to the `while` condition.

<tip-box> 

{{ icon_example }} The code below is for reading three words from the user and printing all three at the end. It uses the `continue` statement to skip the remainder of the iteration if the word entered is too short (i.e., shorter than 4 letters).

```python
accepted_words = ''
count = 0
while count < 3:
  word = input('Enter a word (with 4 letters or more):')
  if len(word) < 4:
    print('Too short. Ignored.')
    continue # skip the remainder of the iteration
  accepted_words = accepted_words + ' ' + word
  count = count + 1
print('Accepted words: ' + accepted_words)
```

<panel type="seamless" header="%%{{ icon_try }} Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/three-words?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} `continue` inside `while` loops%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/885qKiiKisI?rel=0&showinfo=0&start=449&end=545&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Vending Machine - Legit Coins" var-file="e-vending-legitCoins.md" />