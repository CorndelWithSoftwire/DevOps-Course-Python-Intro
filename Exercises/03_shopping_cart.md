# Exercise 2: Shopping Cart

## Introduction
We've learned a bunch of Python now! Concepts like operators, variables, and being able to construct strings and print them to the console allow us to put Python to work in a variety of situations!

As a quick recap:

We can use operators to calculate things, like how much 34 apples would cost if they were £0.42 each:

```
34 * 0.42
```

We can use variables to store results for later:

```
my_apples_cost = 34 * 0.42
```

We can use operators on other types, like strings. Strings support the use of the plus sign to join strings together:

```
greeting = "Hello, " + "Anna"
```

We can call the `print` function, which will then display what we give it to the terminal screen for us to see:

```
greeting = "Goodbye, " + "Anna"
print(greeting)
```

Strings don't, however, support using the plus sign to add them to numbers:

```
age = 39
print("I am " + age + " years old")

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: cannot concatenate 'str' and 'int' objects
```

But since we know the plus sign can join strings together, we just need to turn the number into a string first:

```
age_number = 39
age_string = str(age_number)
print("I am" + age_string + " years old")
```

## Exercise
We have a list of items in a shopping cart. We want to find out the total cost, but it's quite complicated. We need to write a Python script to calculate the cost for us!

We have a shopping cart with:
- 4 apples costing £0.21 each
- 5 bananas costing £0.12 each

This information is provided to your Python code like this:

```
>>> shopping_cart = [{'name': 'apple', 'price_per_item': 0.21, 'number': 4}, {'name': 'banana', 'price_per_item': 0.12, 'number': 5}]
```

To make life complicated, the following rules apply:
- Apples are on sale at 50% off
- There is an additional sales tax for the entire basket of 15%

We want an output of the following form (except with the actual prices instead of £0.00):

```
Cost of basket before sales and tax: £0.00
Cost of basket after sales, before tax: £0.00
Cost of basket after sales and tax: £0.00
```

Write the python code required to perform all the calculations - you'll find it helpful to use variables to store your intermediate results.
Then, use the `print()` function to display the output.

It's okay if your code only works for this specific shopping cart. We will revisit this exercise after chapter 5 to handle a cart of any size and with any items!

## Hints
- I'm getting this error: `TypeError: cannot concatenate 'str' and 'int' objects`
	- You may be trying to use the `+` operator on a string and an integer - remember that `+` can only either add two numbers together (`4 + 4`), or join two strings together (`"Hello, " + "Sarah"`). You might need to use the `str()` function to convert your number into a string first.