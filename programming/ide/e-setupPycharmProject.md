#### Exercise : Setup a Project in PyCharm

1. Install Python and PyCharm if you haven't done so already.
1. Start PyCharm and click on the `Create New Project` option.<br>
   ![]({{ baseUrl }}/programming/ide/images/createNewProject.png)
1. Create a folder for your project. In the next screen, specify that as the project location.<br>
   ![]({{ baseUrl }}/programming/ide/images/specifyProjectLocation.png)
1. You can accept defaults for the remaining steps.
1. To add a new file, right-click on project name and choose `New` → `File`. Provide a file name in the next screen. E.g., `hello.py`<br>
   ![]({{ baseUrl }}/programming/ide/images/addNewFile.png)
1. Type your code in the file.<br>
   ![]({{ baseUrl }}/programming/ide/images/editCode.png)<br>
   Here is an example:
   ```python
   greeting = 'hello'
   
   
   def print_greeting(name):
       message = greeting + ' ' + name
       print(message)
   
   
   print_greeting('john')
   print_greeting('jane')
   ```
1. To run the code, Right-click on project name and choose `Run 'filename'`.<br>
   ![]({{ baseUrl }}/programming/ide/images/runCode.png)
1. The output will appear in the panel at the bottom of the IDE.<br>
   ![]({{ baseUrl }}/programming/ide/images/seeOutput.png)
