#### Exercise : Debug a Project in PyCharm

1. Open a project in PyCharm. Go to a project file containing Python code.
1. To create a breakpoint at a statement, click on the <tooltip content="the area between the statement and the line number">_gutter_</tooltip> next to the line. A red dot should appear to indicate that the breakpoint has been set. %%You can remove the breakpoint by clicking on the red dot again.%%<br>
   ![]({{ baseUrl }}/programming/ide/images/addBreakPoint.png)
1. To start debugging, choose `Debug` instead of `Run.`<br>
   ![]({{ baseUrl }}/programming/ide/images/startDebugging.png)
1. The execution will pause at the first breakpoint. Use the debugging buttons to step through the code. You can see the , choose `Debug` instead of `Run`. You can see the value of the variables in the _debugger_ Window, in the area below the debugging buttons.<br>
   ![]({{ baseUrl }}/programming/ide/images/stepThroughCode.png)<br>
   Useful buttons:<br>
   * `Step over`: executes the statement and moves to the next statement
   * `Step in`: goes into the function that is called in the current statement.
   * `Step out`: finish executing the current function and goes back to the code that called the function.

