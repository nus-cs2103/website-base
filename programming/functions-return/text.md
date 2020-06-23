### Return Value

**You can use a `return` statement to make a function return a value**.

<tip-box> 

{{ icon_example }} The `play()` function below returns one of the strings `Rock`, `Paper`, `Scissors` randomly.

```python
import random

def play():
  value = random.randint(1,3)
  if value == 1:
    return 'Rock'
  elif value == 2:
    return 'Paper'
  else:
    return 'Scissors'
  
print('Player1 response : ' + play())
print('Player2 response : ' + play())
```
<include src="tryYourOwn.md" boilerplate ><span id="program">rps-play-only</span></include>

</tip-box>

**You can use an empty `return` statement to return from the function without executing the remainder of the function**, even if the function does not return anything.

<tip-box> 

{{ icon_example }} The `print_all_products` function below uses an empty `return` statement to return from the function early if one of the arguments is `0`:

```python
def print_product(a, b):
  print(a, 'x', b, '=', a*b)

def print_all_products(n1, n2, n3):
  # return early if any value is 0
  if n1 == 0 or n2 == 0 or n3 == 0:
    print('Values cannot be zeros')
    return
  
  # print all possible products
  print_product(n1, n2)
  print_product(n2, n3)
  print_product(n3, n1)
  
  
print_all_products(2,3,4)
print_all_products(0,2,3)
```
<include src="tryYourOwn.md" boilerplate ><span id="program">print-all-products</span></include>

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Returning values from functions%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/WB4hJJkfhLU?rel=0&showinfo=0&start=315&end=462&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<include src="exercisePanel.md" boilerplate var-title="Grader - `calculate_grade` function" var-file="e-grader-calculateGradeFunction.md" />
