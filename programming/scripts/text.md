### Scripts (Programs)

While the interactive shell is good for testing out small code bits, longer Python programs (also called _scripts_) are written as text files with the `.py` extension. Python _<tooltip content="the tool that interprets the code and executes it">interpreter</tooltip>_ reads the program and executes statements from top to bottom.

Let's create and run a Python program:

<tabs> 
  <tab header="Using repl.it (no need to save as a file)">

Press the :fas-play: button to run the code %%&nbsp;(don't worry about the meaning of the code)%%. You can edit the code and run again!
   
<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/helloworld?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
   
  </tab>
  <tab header="Using IDLE (need to save as a `.py` file)">

1. <trigger trigger="click" for="modal:scripts-openIdle">Open the IDLE tool</trigger>.
1. Choose `File` → `New File`
1. In the new window that opens up, enter the following code %%&nbsp;(don't worry about the meaning of the code)%%.
   ```python
   print('Hello world!')
   print('Bye!')
   ```
1. Save the file by choosing `File` → `Save as`. You can give a name such as `hello.py`
1. `Run` → `Run Module (F5)`. The output will show up in the IDLE shell. 

<panel type="seamless" header="%%{{ icon_video }} Writing your first Python program%%">

<iframe width="560" height="315" src="https://www.youtube.com/embed/buMTH6ICnqk?rel=0&showinfo=0&start=2&end=168&version=3" frameborder="0" allowfullscreen></iframe>

</panel>

  </tab>
</tabs>

<modal large header="{{ icon_video }} Opening IDEL in Windows 10" id="modal:scripts-openIdle">
  
<iframe width="560" height="315" src="https://www.youtube.com/embed/dX2-V2BocqQ?rel=0&showinfo=0&start=247&end=270&version=3" frameborder="0" allowfullscreen></iframe>

</modal>



