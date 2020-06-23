#### Exercise - Vending Machine - Add Loop

The code below simulates a vending machine that asks for a coin and gives out the product and the balance.
```python
price = 100
coin_value = 0

print('Price:', price)

coin_value = int(input('Enter a coin:'))
print('You have entered:', coin_value)

print('Here is the product')
print('Your balance:', coin_value - price)
```
{{ icon_tip }} Note how the above code uses `input` function with a string argument e.g., `input('Enter a coin:')` to show the string to the user and read the input from the user at the same time.

<table>
<tr>
  <td>
  
```python
name = input('Input a name:')
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```
Input a name: John
```
  </td>
</tr>
<tr>
  <td>
  
```python
print('Input a name:')
name = input()
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```
Input a name:
John
```
  </td>
</tr>
</table>

{{ icon_tip }} Also note how the above code uses `print()` with two arguments, one an integer and one a string. The `print()` method can take multiple arguments and the arguments can be of different types. Note that the ==output will have a space between each argument==. 

<table>
<tr>
  <td>
  
```python
print('ABC', 3, 4.50)
print('ABC' + str(3) + str(4.50))
print('ABC' + ' ' + str(3) + ' ' + str(4.50))
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```

ABC 3 4.50
ABC34.50
ABC 3 4.50
```
  </td>
</tr>
</table>

Example output from the code:
```python
Price: 100
Enter a coin: 200
You have entered: 200
Here is the product
Your balance: 100
```

As you can see, this code does not consider the case where the inserted coin is less than the price of the product, resulting in the following incorrect behavior.

```python
Price: 100
Enter a coin: 50
You have entered: 50
Here is the product
Your balance: -50
```

Modify the code to repeat these two lines until the coin entered is enough to pay for the product. Note that you ==don't need to add up all the coins entered.== Instead, assume the vending machine can accept only one coin for a purchase and keeps rejecting coins until a big-enough coin is entered.
```python
coin_value = int(input('Enter a coin:'))
print('You have entered:', coin_value)
```

The output should be something like this:
```python
Price: 100
Enter a coin: 50
You have entered: 50
Enter a coin: 100
You have entered: 100
Here is the product
Your balance: 0
```