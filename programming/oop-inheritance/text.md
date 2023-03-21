### Inheritance

**You can make a class <tooltip content="define a new class based on an existing class">inherit</tooltip> from another class.** If you do, it is as if the <tooltip content="the new class">_child class_</tooltip> already has all the attributes and methods of the <tooltip content="the class that was inherited from">_parent class_</tooltip>.

Syntax:
```python
class ChildClassName(ParentClassName):
  # statements of the class
```

<box>

{{ icon_example }} Consider the `Person` class below:

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
class Person:
  def __init__(self, name):
    self.name = name

  def print_info(self):
    print('My name is', self.name)

amy = Person('Amy')
amy.print_info()
```
</span>
<span id="output">

```{.no-line-numbers}
My name is Amy
```
</span>
</include>

The `Teacher` class below inherits from the `Person` class given above.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python
class Teacher(Person):

  def teach(self):
    print(self.name, 'is teaching')

dan = Teacher('Dan')
dan.print_info()
dan.teach()
print('the name is', dan.name)
```
</span>
<span id="output">

```{.no-line-numbers}
My name is Dan
Dan is teaching
the name is Dan
```
</span>
</include>

Observe how,
 * a `Teacher` object can use the `print_info()` method defined in the parent class.
 * the statement `dan = Teacher('Dan')` invokes the `__init__()` method defined in the parent class too.
 * the statement `print('the name is', dan.name)` is accessing the attribute `name` from a `Teacher` object although the attribute is defined in the parent class.
 * the method `teach` accesses the attribute `name` using `self.name` although the attribute is defined in the parent class.
</box>

<include src="exercisePanel.md" boilerplate var-title="Add `Fish` Class" var-file="e-addFishClass.md" />

**A child class can _override_ a method defined in the parent class.** That way, a child object can change a behavior defined in the parent class.

<box>

{{ icon_example }} Note how the `Student` class below overrides the `print_info()` method of the parent class `Person`.

<include src="inputOutput.md" boilerplate>
<span id="input">
```python{.no-line-numbers}
class Person:
  def __init__(self, name):
    self.name = name

  def print_info(self):
    print(self.name, 'is a person')
```

```python{.no-line-numbers}
adam = Person('Adam')
adam.print_info()
ben = Student('Ben')
ben.print_info()
```
</span>
<span id="output">

```python{.no-line-numbers highlight-lines="2-4"}
class Student(Person):

  def print_info(self):
    print(self.name, 'is a student')
```

<br><br><br>

```{.no-line-numbers}
Adam is a person
Ben is a student
```
</span>
</include>

</box>

When overriding methods, you can reuse the parent's definition of the same method using the `super().` prefix.

<box>

```python
class Person:
  def __init__(self, name):
    self.name = name
```
{{ icon_example }} Given that `Person` class has the initializer method given above, the following two versions of the `Student` class are equivalent.

(a) Override without reusing parent's method
```python{.no-line-numbers}
class Student(Person):
  def __init__(self, name, matric):
    self.name = name
    self.matric = matric
```

(b) Override but reuse parent's method (preferred)
```python{.no-line-numbers highlight-lines="3"}
class Student(Person):
  def __init__(self, name, matric):
    super().__init__(name) # reuse parent's method
    self.matric = matric
```

</box>

<include src="exercisePanel.md" boilerplate var-title="Add `FlightlessBird` Class" var-file="e-addFlightlessBirdClass.md" />

**Note that all python classes automatically inherits from the built-in class `object`** even if you did not specify it as the parent class. The `object` class has a `__str__()` method that you can ovrride in your classes to customize how the `print` function will print an object of your class.

<box>

{{ icon_example }} The `Book` class below overrides the `__str__()` method so that `Book` objects can be printed in a specific format.

<include src="inputOutput.md" boilerplate>
<span id="input">

```python{highlight-lines="5-6,9"}
class Book:
  def __init__(self, title):
    self.title = title

  def __str__(self):
    return 'Book title: ' + self.title

book = Book('Python for Beginners')
print(book)
```
</span>
<span id="output">

```{.no-line-numbers}
Book title: Python for Beginners
```
</span>
</include>

</box>

<include src="exercisePanel.md" boilerplate var-title="Override `__str__()` Method" var-file="e-overrideStr.md" />


**A class can inherit from multiple classes.** If multiple parent classes have the same method, the one that is given first (in the order of inheritance) will be used.

<box>

<include src="inputOutput.md" var-arrow="" boilerplate>
<div id="input">

```python{.no-line-numbers}
class Person:
  def __init__(self, name):
    self.name = name

  def print_info(self):
    print('My name is', self.name)
```
```python{.no-line-numbers}
class Teacher(Person):

  def teach(self):
    print(self.name, 'is teaching')

  def print_info(self):
    print(self.name, 'is a teacher')

```
</div>
<div id="output">

```python{.no-line-numbers}
class Student(Person):
  def __init__(self, name, matric):
    super().__init__(name)
    self.matric = matric

  def learn(self):
    print(self.name, 'is learning')

  def print_info(self):
    print(self.name, 'is a student')
```
```python{.no-line-numbers highlight-lines="1"}
class TeachingAssistant(Teacher, Student):

  def grade(self):
    print(self.name, 'is grading')
```
</div>
</include>

{{ icon_example }} The `TeachingAssistant` class above inherits from both `Student` class and the `Teacher` class both of which inherit from the `Person` class. That means a `TeachingAssistant` object can use methods from classes `object`, `Person`, `Student`, `Teacher`, and `TeachingAssistant`.

<table>
<tbody>
<tr>
<td>

```python
elsie = TeachingAssistant('Elsie', 'A223344')
elsie.print_info()
elsie.teach()
elsie.learn()
elsie.grade()
```
</td>
<td valign="bottom">&nbsp;→&nbsp;<br><br></td>
<td valign="bottom">

```{.no-line-numbers}
Elsie is a teacher
Elsie is teaching
Elsie is learning
Elsie is grading
```
</td>
</tr>
</tbody>
</table>

As both `Teacher` and `Student` classes have the `print_info()` method, the method from the `Teacher` class will be used as it comes first in the inheritance order `(Teacher, Student)`; that is why you see `Elsie is a teacher` in the output instead of `Elsie is a student`.

</box>

<include src="exercisePanel.md" boilerplate var-title="Add `SmartPhone` Class" var-file="e-addSmartPhoneClass.md" />

**You need to use inheritance when you create user-defined exceptions because** all such exceptions need to inherit from a built-in `Exception` class.

<box>

{{ icon_example }} In the example below, `EmptyCommandError` and `InvalidCommandError` are user-defined exceptions. The latter has overridden the constructor to take additional parameters.

```python{highlight-lines="1,6"}
class EmptyCommandError(Exception):
    """Indicates a task has expired."""
    pass


class InvalidCommandError(Exception):
    """Indicates that the user entered an invalid command"""

    def __init__(self, command, explanation):
        self.command = command
        self.explanation = explanation


def execute_command(command):
    if command == '':
        raise EmptyCommandError()
    elif len(command) < 4:
        raise InvalidCommandError(command, "command too short")


def process(command):
    try:
        execute_command(command)
    except EmptyCommandError:
        print('empty command')
    except InvalidCommandError as e:
        print('invalid command:', e.command, '->', e.explanation)


process('')
process('HA')
```
{{ icon_output }}
```{.no-line-numbers}
empty command
invalid command: HA -> command too short
```
</box>
