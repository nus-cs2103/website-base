### Local and Global Scope

**The _scope_ of a variable is which part of the code it can be read/modified.** Think of a scope as a container for variables. When a scope is destroyed, all the values stored in the scope’s variables are forgotten.

**The _global scope_ is the scope that is applicable to the entire program.** There is only one global scope, and it is created when your program begins. When your program terminates, the global scope is destroyed, and all its variables are forgotten. Otherwise, the next time you ran your program, the variables would remember their values from the last time you ran it. **A variable that exists in the global scope is called a _global variable_.**

**A _local scope_ is a scope that applies only during the execution of a function.** A local scope is created whenever a function is called. Parameters and variables that are assigned in the called function are said to exist in that function’s local scope. **A variable that exists in a local scope is called a _local variable_.** When the function returns, the local scope is destroyed, and these variables are forgotten. The next time you call this function, the local variables will not remember the values stored in them from the last time the function was called.

A variable must be in the global scope or the local scope; it cannot be in both. 

<sub>%%[Some parts of the above explanation were adapted from [_Automate the Boring Stuff_](https://automatetheboringstuff.com/chapter3/)]%%</sub>

Consider the code given below %%(apparently, from a program related to a farm)%%. The global scope and the local scope of each function indicated by shaded areas.<br>
<img src="{{baseUrl}}/programming/functions-scope/images/scopeAsShadedAreas.png" width="500" />

Note the following rules about scope:
* Rule 1: **Local scopes can read global variables** e.g., `raise_chicken` function can access the global variable `total_chickens` (see line 6).
* Rule 2: **Global scope cannot read/write local variables** e.g., line 11 will be rejected because it reads the local variable `eggs`.
* Rule 3: **Local scopes cannot read/write variables of other local scopes** e.g., line 15 will be rejected because it reads the local variable `eggs`.
* Rule 4: **If a variable is ==_assigned_== in a local scope, it becomes a local variable** even if a global variable has the same name. That is, there can be separate global and local variables with the same name.  e.g., line 16 (`total_cows = 10`) creates a local variable `total_cows` although there is also a global variable `total_cows`; the line 19 prints `5` because the `total_cows` global variable remains `5` and the local variable `total_cows` which has the value `10` is destroyed after the function `milk_cows` is executed.

**To modify a global variable within a local scope, use the `global` statement on that variable.**

<tip-box> 

{{ icon_example }} The `breed_cows` function below can increase the global variable `total_cows` to `10` from the local scope because it has a `global total_cows` statement. If you remove that statement, the last print statement will print `5` instead of `10`

```python
total_cows = 5
print('total cows before breeding:', total_cows)

def breed_cows():
    global total_cows
    print('breeding cows')
    total_cows = 10
    print('total cows at the end of breeding:', total_cows)

breed_cows()
print('total cows after breeding:', total_cows) # prints 10
```

<table>
<tr>
  <td>
  
{{ icon_output }}
```
total cows before breeding: 5
breeding cows
total cows at the end of breeding: 10
total cows after breeding: 10
```
  </td>
  <td>&nbsp;&nbsp;</td>
  <td>
 
{{ icon_output }} without the `global total_cows` statement
```
total cows before breeding: 5
breeding cows
total cows at the end of breeding: 10
total cows after breeding: 5
```
  </td>
</tr>
</table>

<include src="tryYourOwn.md" boilerplate var-program="functions-breedCows" />

</tip-box>

<include src="exercisePanel.md" boilerplate var-title="Grader - Add `main` Function" var-file="e-grader-addMainFunction.md" />
<include src="exercisePanel.md" boilerplate var-title="Grader - Restructure the `main` Function" var-file="e-grader-restructureTheMainFunction.md" />
<include src="exercisePanel.md" boilerplate var-title="Grader - Analyze Grades in a Loop" var-file="e-grader-analyzeInLoop.md" />



