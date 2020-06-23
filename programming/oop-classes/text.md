### Classes

**You can define your own _classes_ (i.e., object types)** in Python, which can then be used alongside the built-in classes such as `list`, `int`, `str`, etc.

The syntax for defining a class:
```python
class ClassName:
  # <statement-1>
  .
  .
  .
  # <statement-N>
```
{{ icon_tip }} It is customary to use <trigger trigger="click" for="modal:classes-camelcase">Upper Camel Case</trigger> for class names.

The syntax for **creating (also called _instantiating_) an object** of the class is `ClassName()`.

<modal header="CamelCase" id="modal:classes-camelcase">

![](https://upload.wikimedia.org/wikipedia/commons/e/ef/CamelCase.svg =200x)<br>

Camel Case refers to a styling text writing compound words or phrases such that each word or abbreviation in the middle of the phrase begins with a capital letter, with no intervening spaces or punctuation e.g., `freshAppleJuice`. _Upper Camel Case_ (also called _Pascal Case_) is similar to Camel Case except the first letter is capitalized as well e.g., `FreshAppleJuice`.

<sub>[source: [Wikipedia](https://en.wikipedia.org/wiki/Camel_case)]</sub>
</modal>

<box> 

{{ icon_example }} The code below defines a class named `Employee`, creates two employee objects, and prints the class/type of each object.

```python
class Employee:
  pass # an empty class

john = Employee() # create an Employee object
print(type(john)) # print type of the john object
alice = Employee()
print(type(alice))
```
{{ icon_output }} %%Note how the type of each object is given as `<class 'Employee'>` i.e., a class with name `Employee`.%%
```
<class 'Employee'>
<class 'Employee'>
```
</box>

**You can add methods to the class by defining them inside the class definition.** Note that a method of a class always take `self` as the first parameter. `self` refers to the object itself. When calling the method, there is no need to supply an argument for the `self` parameter as the target object is implicitly taken as the argument for that parameter.

<box> 

{{ icon_example }} Consider the code below:

<include src="inputOutput.md" boilerplate> 
<span id="input">

```python
class Pen:
  
  def write(self, text):
    print('writing:', text)
    
p = Pen()
p.write('It was a dark night ...')
```
</span>
<span id="output">

```
writing: It was a dark night ...
```
</span>
</include>

`write(self, text)` method is called as `p.write('It was a dark night ...')`.<br>
This is how the arguments are matched with the parameters: 
* `self` → `p`
* `text` → `'It was a dark night ...'`

</box>

**You can specify how to initialize an object of a class by defining an `__init__()` method in the class.** Here are the important things to note about the `__init__()` method: 
1. There are two underscores in front and two behind the word `init`.<br>
   {{ icon_x_red }} `_init_(self)`<br>
   {{ icon_tick_green }} `__init__(self)`
1. It will be called every time you create an instance of the class.
1. If it has parameters, you need to provide arguments for those parameters when you instantiate an object of that class.

<box> 

{{ icon_example }} This example shows an `__init__` method added to a `Person` class.

<include src="inputOutput.md" boilerplate> 
<span id="input">

```python
class Person:
  
  def __init__(self, name):
    print(name, 'initialized!')
    
tom = Person('Tom')
```
</span>
<span id="output">

```
Tom initialized!
```
</span>
</include>

</box>

**An object can have _attributes_** i.e., values attached to the object, just as an object can have methods. Attributes and methods of an object can be accessed using the `objectname.` syntax, as you did with objects of built-in classes.

<box> 

{{ icon_example }} This example shows accessing the `get_age()` method and the `birthday` attribute of an object `x`.

<include src="inputOutput.md" boilerplate> 
<span id="input">

```python
print(x.get_age())
print(x.birthday)
```
</span>
<span id="output">

```
12
01/11/2000
```
</span>
</include>

</box>

**The code within a class needs to use the `self.` to refer to its own attributes and methods.** Furthermore, the best place to initialize attributes is the `__init__()` method.

<box> 

{{ icon_example }} Note how the `__init__()` method of the `Book` class initializes its two attributes and calls another of its own methods i.e., `self.describe()`.

```python
class Book:
  
  def __init__(self, book_title, book_author):
    self.title = book_title # initialize attribute title
    self.author = book_author # initialize attribute author
    self.describe() # call another method of the class
    
  def describe(self):
    # print attributes of the object
    print('Book info:', self.title, '/by', self.author) 
    
book1 = Book('The Jungle Book', 'Leo Tolstoy')
book2 = Book('The Art of War', 'Sun Tzu')

print()  # print a blank line
print('Title:', book1.title) 
print('Author:', book1.author)
book1.describe()
```
{{ icon_output }}
```
Book info: The Jungle Book /by Leo Tolstoy
Book info: The Art of War /by Sun Tzu

Title: The Jungle Book
Author: Leo Tolstoy
Book info: The Jungle Book /by Leo Tolstoy
```
</box>

**You can get your classes to work with each other.**

<box> 

{{ icon_example }} In this example we define a `ReadingList` class that can store a list of `Book` objects.

```python
class ReadingList:
  
  def __init__(self, initial_list):
    self.books = initial_list
    
  def add_book(self, book):
    self.books.append(book)
    
  def show_authors(self):
    for b in self.books:
      print(b.author)
      
my_list = ReadingList([book1]) # book1 defined in a previous example 
my_list.add_book(book2) # book2 defined in a previous example
my_list.show_authors()
```
{{ icon_output }}
```
Leo Tolstoy
Sun Tzu
```
</box>

<include src="exercisePanel.md" boilerplate var-title="Create `StockItem` Class" var-file="e-createStockItemClass.md" />