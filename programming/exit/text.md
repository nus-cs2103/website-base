### Early Termination

At times you may need to terminate a program execution early %%&nbsp;i.e., without reaching the end of the code%%. **You can use the `exit()` function in the `system` module to terminate a program early.**
 

<tip-box> 

{{ icon_example }} The code below prints out the factorials of `1` to `n` where `n` is specified by the user. If `n` is `0`, it uses `sys.exit()` to terminate the program immediately.

```python
import math, sys

n = int(input('Number of factorials (0 to exit):'))

if n == 0:
  print('Terminating as requested...')
  sys.exit()
  
for i in range(n):
    print(math.factorial(i+1)) # use i+1 because i starts from 0
```

<panel type="seamless" header="%%{{ icon_try }} Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/print-factorials?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%{{ icon_video }} Early termination%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/xJLj6fWfw6k?rel=0&showinfo=0&start=155&end=223&version=3" frameborder="0" allowfullscreen></iframe>

</panel>
 

