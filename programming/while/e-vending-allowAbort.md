#### Exercise - Vending Machine - Allow Abort

The vending machine you wrote in the previous exercise (an example solution given below) does not allow the user to abort the purchase and get the money back.
```python
price = 100
coin_sum = 0

print('Price:', price)

while price > coin_sum:
  coin_value = int(input('Enter a coin:'))
  coin_sum = coin_sum + coin_value
  print('You have entered:', coin_sum)

print('Here is the product')
print('Your balance:', coin_sum - price)
```

Modify the code so that the user can abort the purchase by entering `0` as the coin value:

```python
Price: 100
Enter a coin: 20
You have entered: 20
Enter a coin: 0
Your balance: 20
```

<include src="seeHint.md" boilerplate >
<span id="hint_body">

```python
...
is_aborting = False
...
  if coin_value == 0:
    is_aborting = True
    break
... 
if is_aborting:
  print('Your balance:', coin_sum)
```
</span>
</include>