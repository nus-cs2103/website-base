#### Exercise - Vending Machine - Accept Multiple Coins

The vending machine you wrote in the previous exercise (an example solution given below) can accept only one coin as the payment. If the coin is not enough, it rejects the coin and request the user to insert a new coin.
```python
price = 100
coin_value = 0

print('Price:', price)

while price > coin_value:
  coin_value = int(input('Enter a coin:'))
  print('You have entered:', coin_value)

print('Here is the product')
print('Your balance:', coin_value - price)
```

Modify the code so that it can accumulate coins until there is enough to pay for the product. An example output is given below:

```python
Price: 100
Enter a coin: 20
You have entered: 20
Enter a coin: 50
You have entered: 70
Enter a coin: 50
You have entered: 120
Here is the product
Your balance: 20
```

<include src="seeHint.md" boilerplate >
<span id="hint_body">

```python
...
coin_sum = 0
...
  coin_sum = coin_sum + coin_value
...
```
</span>
</include>