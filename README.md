# PREVPAPERS
<h1>Welcome to my Repo</h1>
prevpapers is a educational website, From there, usr can get access of the a lot of study materials and epapers. 
Download free epapers and free <a href="https://prevpapers.com/">previous year question paper. </a>
<a href="https://epapers.prevpapers.com/">Free download Epaper PDF online</a>
<a href="http://mateshwarionewaytaxi.in/">Best one way taxi service in udaipur</a>
https://prevpapers.com/


Aaron adds some syntactic sugar to Python function composition.

## How?

Say you have the following functions:

```python
def add_one(n):
    return n + 1

def double(n):
    return n * 2

def ints_less_than(n):
    return range(1,n)

def product(*ns):
    result = 1
    for n in ns:
        result *= n

    return result
```

You could do something like this:

```python
def two_n_plus_one(n):
  return add_one(double(n))

def product_of_lesser_numbers(n):
  return product(*ints_less_than(n))
```

Or, you could use Aaron, decorate your functions with `composable`, and do this:

```python
two_n_plus_one = double > add_one

product_of_lesser_numbers = ints_less_than >> product
```

You've probably figured out by now that `>` is composition, and `>>` is will
splat the results into the next function.

## Aaron? What?

Yeah, the [composer](http://en.wikipedia.org/wiki/Aaron_Copland). Get it?
