## Appendix D: Unit Testing

The built-in module `unittest` supports automation of unit testing in an object-oriented way.

Let's assume you have a file called `search.py` which has the following two functions.

```python{heading="in search.py"}
def get_first_name(name):
  """Return the first part of the parameter 'name'"""
  return name.split()[0]


def is_same_person(person, keyword):
  """Return True if the parameter 'person' (type: dictionary)
  contains a key 'name' whose value contains the 
  parameter 'keyword' (type: string)
  e.g., 
  * is_same_person({'name': 'jackie'}, 'jack') returns True
  * is_same_person({'name': 'jackie'}, 'jackie-chan') returns False
  """
  return keyword in person['name']
```

This is how we can write some unit tests for the two functions.

```python{heading="in test_search.py"}
import search, unittest

class TestSearch(unittest.TestCase):

  def test_is_same_person(self):
    jack = {'name':'jack'}
    self.assertTrue(search.is_same_person(jack, 'jack'))
    self.assertTrue(search.is_same_person(jack, 'ack'))
    self.assertTrue(search.is_same_person(jack, 'ac'))
    self.assertTrue(search.is_same_person(jack, 'j'))
    self.assertTrue(search.is_same_person(jack, 'k'))
    self.assertFalse(search.is_same_person(jack, 'jackie'))
    self.assertFalse(search.is_same_person(jack, 'blackjack'))
    self.assertFalse(search.is_same_person({'name': 'x', 'other': 'jack'}, 'jack'))
    with self.assertRaises(KeyError):
      search.is_same_person({}, 'jack')
  
  def test_get_first_name(self):
    self.assertEqual(search.get_first_name('Amy'), 'Amy')
    self.assertEqual(search.get_first_name('Amy Bernice'), 'Amy')
    self.assertEqual(search.get_first_name('Amy-Bernice'), 'Amy-Bernice')
    with self.assertRaises(IndexError):
      search.get_first_name('')

# activate the test runner
if __name__ == '__main__':
    unittest.main()
```
When you run the above code, each method in the test class will be executed by a built-in _test runner_ and the result will be reported. An example is given below:
```{.no-line-numbers}
...
----------------------------------------------------------------------
Ran 2 tests in 0.019s

OK
```

Things to note:
* A class containing unit tests should inherit from `unittest.TestCase`
* Names of functions containing test code should start with `test` e.g., `test_is_same_person()`
* These methods (inherited from the parent class) can be used to compare actual with the expected value:
  * `assertTrue(actual)` : test passes if `actual == True`
  * `assertFalse(actual)` : test passes if `actual == False`
  * `assertEquals(actual, expected)` : test passes if `actual == expected`
  * `with self.assertRaises(Exception):` passes if the code block it contains raises the specified exception.  

If the expected value is not as same as the actual, the test runner will report the test failure. For example, if we were to insert this statement into `test_get_first_name` method,
```python{.no-line-numbers}
self.assertEqual(search.get_first_name('Amy Foo'), 'Foo')
```
the output will be something like this:
```{.no-line-numbers}
F.
======================================================================
FAIL: test_get_first_name (__main__.TestSearch)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "main.py", line 19, in test_get_first_name
    self.assertEqual(search.get_first_name('Amy Foo'), 'Foo')
AssertionError: 'Amy' != 'Foo'
- Amy
+ Foo


----------------------------------------------------------------------
Ran 2 tests in 0.001s

FAILED (failures=1)
```

:paperclip: Resources:
* More on unit testing: [https://docs.python.org/3/library/unittest.html](https://docs.python.org/3/library/unittest.html)
* Unit testing in the PyCharm IDE: [https://www.youtube.com/watch?v=-VzJvNLooj4](https://www.youtube.com/watch?v=-VzJvNLooj4)