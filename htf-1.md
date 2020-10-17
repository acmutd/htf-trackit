# Launch Notebook

Click the button below to launch this workshop's notebook in Google Colaboratory, an online environment for Python.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/acmutd/htf-research/blob/main/starter-notebook.ipynb)


# Libraries

*Libraries* are reusable bits of code that help you achieve certain tasks. For example, in this workshop, we're using the yfinance library to download stock data from Yahoo Finance.

Some other examples of libraries we'll be using in this workshop include Pandas and Matplotlib.

# Dictionaries

*Dictionaries* allow you to access different values by using a string, called a key. Dictionaries are also called hashmaps in other programming languages. Dictionaries are really useful when grouping related values together:

```python
money_owed = {
	'john': 20,
	'jack': 5,
	'lisa': 12
}

print(money_owed['lisa']) # prints 12

```

# String Interpolation

*String interpolation* allows you to insert values into strings without needing to combine multiple smaller strings together. Here's an example where string interpolation is useful:

```python
name = 'John'
preferred_drink = 'Vanilla Cold Brew'
uber_eta = 10


# Before
print('Hello, ' + name + '! Your ' + preferred_drink + ' is on the kitchen counter and your Uber arrives in ' + uber_eta + ' minutes.')

# After
print(f'Hello, {name}! Your {preferred_drink} is on the kitchen counter and your Uber arrives in {uber_eta} minutes.')
```