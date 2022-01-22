#### Exercise : `StockItem` with Price

Enhance the `StockItem` class you wrote in the previous exercise so that each `StockItem` object can keep track of its own price and the price can be increased later.

<table>
<tr>
  <td>

```python
# ADD StockItem class here
# It should have attributes: name, price
# It should have methods: info, increase_price

items = []
items.append(StockItem('Pen', 5))  # a pen worth 5 dollars
items.append(StockItem('Pencil', 3))
items.append(StockItem('Cup', 1))
for item in items:
    item.increase_price(1)  # increase price by 1
    print(item.info())
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom"> 

```{.no-line-numbers}
The price of Pen is 6
The price of Pencil is 4
The price of Cup is 2
```
  </td>
</tr>
</table>
