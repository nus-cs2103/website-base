### `if` Statements

Python uses the `if` statement to indicate that some code should only be executed if a certain condition is true.

Format:
```
if condition :
    statements_to_execute_if_true
```

{{ icon_example }} The code below has two `if` statements; one evaluates to `true` while the other doesn't.

<div class="container">
 <div class="row">
  <div class="col">

```python
price = 55
print(price)
if price > 50:
    print('Expensive')

weight = 45
print(weight)
if weight > 100:
    print('Heavy')

print('Done')
```

  </div>
  <div class="col align-self-end">

output :fas-level-down-alt:
```
50
Expensive
45
Done
```
<include src="visualize.md" boilerplate >
  <span id="code">price%20%3D%2055%0Aprint%28price%29%0Aif%20price%20%3E%2050%3A%0A%20%20%20%20print%28'Expensive'%29%0Aweight%20%3D%2045%0Aprint%28weight%29%0Aif%20weight%20%3E%20100%3A%0A%20%20%20%20print%28'Heavy'%29%0Aprint%28'Done'%29</span>
</include>

  </div>
 </div>
</div>

Note how the code that should execute when the condition is true is indented (usually by 4 spaces). **Python uses indentation to indicate code _blocks_** (aka _clauses_) %%i.e., a sequence of statements that belong together%%. In the example below, lines 2-4 are in the same block because they are all indented by one level; if the condition is true, all three are executed; if the condition is false, all three are omitted. Line 5 goes back to the previous indentation level, indicating the end of the code block.

```python
if name == 'Blue':          # line 1
    print("It's a color")   # line 2
    print("It's a feeling") # line 3
    print("It's a word")    # line 4
print('Done')               # line 5
```

<include src="exercisePanel.md" boilerplate var-title="Even Numbers" var-file="e-even.md" />

`if` statements can be <tooltip content="one _if_ statement within another">nested</tooltip>, using deeper indentation.

```python
age = 13
gender = 'F'
if (age > 12) and (age < 20):          
    print('Teenager')  # indented one level - new code block starts here 
    if gender == 'F':
        print('Female')# indented two levels - this block is nested within the first block
        print('Girl')  
    if gender == 'M':
        print('Male') # another block nested within the first block
        print('Boy')
    print('Gender code is ' + gender) 
print('Age is ' + str(age))               
```
{{ icon_output }} <include src="visualize.md" boilerplate inline>
  <span id="code">age%20%3D%2013%0Agender%20%3D%20'F'%0Aif%20%28age%20%3E%2012%29%20and%20%28age%20%3C%2020%29%3A%20%20%20%20%20%20%20%20%20%20%0A%20%20%20%20print%28%22Teenager%22%29%20%20%23%20indented%20one%20level%20-%20new%20code%20block%20starts%20here%20%0A%20%20%20%20if%20gender%20%3D%3D%20'F'%3A%0A%20%20%20%20%20%20%20%20print%28'Female'%29%23%20indented%20two%20levels%20-%20this%20block%20is%20nested%20within%20the%20first%20block%0A%20%20%20%20%20%20%20%20print%28'Girl'%29%20%20%0A%20%20%20%20if%20gender%20%3D%3D%20'M'%3A%0A%20%20%20%20%20%20%20%20print%28'Male'%29%20%23%20another%20block%20nested%20within%20the%20first%20block%0A%20%20%20%20%20%20%20%20print%28'Boy'%29%0A%20%20%20%20print%28'Gender%20code%20is%20'%20%2B%20gender%29%20%0Aprint%28'Age%20is%20'%20%2B%20str%28age%29%29%20</span>
</include>

```python
Teenager
Female
Girl
Gender code is F
Age is 13
```

<panel type="seamless" header="%%{{ icon_video }} Using `if`%%">

<iframe width="560" height="315" src="https://www.youtube.com/embed/lWeCgEbk-Ro?rel=0&showinfo=0&start=7&end=253&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

If a situation has only two <tooltip content="no more than one of them can be true at any time">mutually exclusive</tooltip> possibilities %%e.g. if we assume the value of `gender` can only be `M` or `F`%%, we can use the `else` statement to deal with both conditions together.

{{ icon_example }} In the example below, the entire `else` block will be skipped if the `if` condition is true.
```python
if gender == 'F':
    print('Female')
else:
    print('Not Female')               
```
<panel type="seamless" header="%%{{ icon_video }} Using `else`%%">

<iframe width="560" height="315" src="https://www.youtube.com/embed/lWeCgEbk-Ro?rel=0&showinfo=0&start=254&end=336&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

If a situation has more than two mutually exclusive possibilities, we can bring in `elif` (an abbreviation of _else if_) blocks too.

{{ icon_example }} The example below shows how to use an `if-elif-else` construct to control the flow of the execution.
```python
if gender == 'F':
    print('Female')
elif gender == 'M':
    print('Male')
elif gender == 'O':
    print('Other')
else:
    print('Unrecognized value')             
```
<panel type="seamless" header="%%{{ icon_try }} Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/gender-if?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

Note that in an `if-elif-else` construct no more than one block (the first one whose condition is true) will be executed.

<panel type="seamless" header="%%{{ icon_video }} Using `elif`%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/lWeCgEbk-Ro?rel=0&showinfo=0&start=354&end=483&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Grade Analyzer" var-file="e-grades.md" />
<include src="exercisePanel.md" boilerplate var-title="Grade Analyzer (extended)" var-file="e-gradeAnalyzerExtended.md" />