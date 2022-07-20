## Tip Calculator

# Problem Input

If the bill was $150.00, split between 5 people, with 12% tip. 

Each person should pay (150.00 / 5) * 1.12 = 33.6

Format the result to 2 decimal places = 33.60

Thus everyone's share of the total bill is $30.00 plus a $3.60 tip.

# Example Input

```
Welcome to the tip calculator!
What was the total bill? $124.56
How much tip would you like to give? 10, 12, or 15? 12
How many people to split the bill? 7
```

# Example Output

```
Each person should pay: $19.93
```

# Solution

```print("Welcome to the tip calculator!")
bill = float(input("What was the total bill? :"))
tip = int(input("How much tip would you like to give? 10, 12, or 15?"))
people = int(input("How many people to split the bill?"))
total = tip/100 * bill + bill

print(f"Each person should pay: ${total}")
```