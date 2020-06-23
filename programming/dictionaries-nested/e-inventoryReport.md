#### Exercise : Inventory Report

Write a function that prints an inventory report like the examples given below, when the report title (a string), print-width (an int), and list of items (as a suitable data structure, e.g., dictionary) is given to the function.

<box>

{{ icon_example }} Kitchen Inventory Report:

* Title: Kitchen
* Width: 15

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

Item | count
---- | ----
pots | 5
eggs | 100
</span>
<span id="output">

```
###############
### KITCHEN ###
###############
eggs.......:100
pots.......:  5
            ---
total......:105
            ===
```
</span>
</include>

</box>

<box>

{{ icon_example }} Bookshop Inventory Report:

* Title: Book Shop
* Width: 25

<include src="inputOutput.md" var-align="middle" boilerplate>
<span id="input">

Item | count
---- | ----
pens | 85
books | 3
pencils | 22
</span>
<span id="output">

```
#########################
####### BOOK SHOP #######
#########################
books................:  3
pencils..............: 22
pens.................: 85
                      ---
total................:110
                      ===
```
</span>
</include>

</box>

* Title should be centered and in upper case.
* Items should be in alphabetical order.
* Width of the number column is 3. Numbers should be right-justified.


<panel type="seamless" header="%%:bulb: (Python) Partial solution%%">

This exercise requires string formatting methods you learned in an earlier lesson.

```python
def print_inventory(items, title, width):
  print_header(width, title)
  for k in sorted(items.keys()):
    print_item(k, items[k], width)
  print_total(calculate_total(items), width)


def print_header(width, title):
  """ print the given title in the format of a banner.

  Example: print_header(10, 'hi')
  ##########
  ### HI ###
  ##########

  * The title is center aligned and in upper case

  Arguments:
  word -- (type:string) the title of the banner
  width -- (type:int) the width of the banner
  """
  print('#'*width)
  # ADD YOUR CODE HERE


def print_total(total, width):
  """ print the given total in the following format

  Example: print_total(5, 12)
           ---
  total...:  5
           ===

  * The total is right-justified

  Arguments:
  total -- (type:int) the total to print
  width -- (type:int) the width to use for printing
  """
  print('---'.rjust(width, ' '))
  # ADD YOUR CODE HERE


def print_item(name, count, width):
  """ Print the name and count as a row in the inventory listing.

  Example: print_item('pins', 2, 12)
  pins....:  2

  * The count is right-justified in a column that is 3 characters wide.

  Arguments:
  name -- (type:string) name of the item
  count -- (type:int) number of items
  width -- (type:int) the width to use for printing
  """
  pass #  REPLACE WITH YOUR CODE


def calculate_total(items):
  total = 0
  for v in items.values():
    total = total + v
  return total

print_inventory({'pots':5, 'eggs':100}, 'Kitchen', 15)
print('\n')
print_inventory({'pens': 85, 'books': 3, 'pencils': 22}, 'Book Shop', 25)
```

</panel>