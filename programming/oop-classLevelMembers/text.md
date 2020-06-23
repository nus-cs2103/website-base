### Class-Level Members

**Attributes initialized inside a class but outside of its methods are considered class-level attributes** (attributes are also called _data_ or _variables_) i.e., they are shared among all objects of that class whereas attributes initialized inside the `__init__()` method are instance-level attributes i.e., their values vary from instance-to-instance. A class-level attribute is accessed using the `ClassName.` syntax.

<box> 

{{ icon_example }} The `Student` class below has one class-level attribute `total_students`. As it is meant to track the total number of `Student` objects created, it is incremented in the `__init__()` method. `course_count` and `name` are instance-level attributes.

```python{highlight-lines="3,7"}
class Student:
  
  total_students = 0 # class-level attribute
  
  def __init__(self, student_name):
    self.name = student_name # instance-level attribute
    Student.total_students = Student.total_students + 1 # update class-level attribute
    self.course_count = 0 # instance-level attribute
```
The code below creates two `Student` objects. Note how the class-level attribute `total_students`,
 * can be accessed using the class name (i.e., `Student.total_students`) or the object (i.e., `amy.total_students`) and both give the same value.
 * is shared among all objects and correctly gives `2` after another `Student` object has been created.
```python{highlight-lines="2,7"}
amy = Student("Amy")
print('total students:', Student.total_students) # access via class name
print('total students:', amy.total_students) # access via object
print('Amy course count:', amy.course_count)

ben = Student("Ben")
print('total students:', Student.total_students)
print('total students:', ben.total_students) 
print('Ben course count:', ben.course_count)
```
{{ icon_output }}
```{.no-line-numbers}
total students: 1
total students: 1
Amy course count: 0
total students: 2
total students: 2
Ben course count: 0
```
</box>

**It is possible to have class-level methods too.** A class-level method definition should be annotated using a `@classmethod` annotation. In addition, **a class-level method's first parameter should be `cls` which represents the class itself** %%(similar to instance level methods' first parameter needing to be `self`)%%.

<box> 

{{ icon_example }} The `Printer` class below has a class-level attribute `enabled` and class-level methods `enable()` and `disable()`.

```python{highlight-lines="3,12-15,17-20"}
class Printer:

  enabled = True

  def __init__(self, new_text):
    self.text = new_text

  def print_text(self):
    if Printer.enabled:
      print(self.text)

  @classmethod
  def disable(cls):
    cls.enabled = False  # cls here is same as Printer
    print('All Printers disabled')

  @classmethod
  def enable(cls):
    cls.enabled = True
    print('All Printers enabled')
```
The code below uses the class-level method to enable/disable printing for all `Printer` objects.

<include src="inputOutput.md" boilerplate> 
<span id="input">

```python
Printer.disable()
p1 = Printer('blah blah')
p2 = Printer('yak yak')
p1.print_text() # will not print
p2.print_text() # will not print

Printer.enable() 
p1.print_text()
p2.print_text()
```
</span>
<span id="output">

```{.no-line-numbers}
All Printers disabled
All Printers enabled
blah blah
yak yak
```
</span>
</include>

{{ icon_tip }} As you can see from the above code, class-level methods can be called even before any objects of that class have been created.
</box>

<include src="exercisePanel.md" boilerplate var-title="Add Class-Level Members to `Subject` Class" var-file="e-addClassLevelMembersToSubjectClass.md" />