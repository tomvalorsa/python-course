# Session 3 Problems

In session 3 we learned convenient ways to store your data using:

1. Lists
2. Dictionaries

## A little theory

Try to answer the questions then use the python console to check. 

For the following questions assume `L = [0,1,2,3,4]`

- What is `[]`?
- What does `L[-1]` evaluate to?
- What does `L.append(9)` make the list `L` look like?
- What does `L.insert(2,9)` make the list `L` look like?

For the following questions assume `L = ["alex", "mia", "john", "laura", "joyce"]`

- What does `L.pop()` *return* and what does the list `L` become?
- What does `L.remove("mia")` *return* and what does the list `L` become?

For the following questions assume `D = {"name":"Alex", "age":27, "height":158}`

- How would you change the value associated with the key `"name"` from "Alex" to "John"?
- How would you add the key-value pair `{"graduate":True}` to the dictionary `D`?
- What would `list(D.keys())` look like?


## Data analysis

For the following list:
```py
# Copy and paste into your script
L = [12,356,321,13,6,-23,-5,35,-424,-2425,45,23,642,634]
```

- Calculate the length of `L`
- Calculate the sum of all elements in `L`
- Find the maxium value
- Find the minium value
- Calculate the mean value (mean = sum of L divided by the number of elements in L)

*Hint:* The `for` loop is very useful when dealing with lists. Below is an example of using a `for` loop to determine the longest name in a list of names.

```py
names = ["Alex", "Mia", "John", "Laura", "Joyce"]
longestName = "" # initialise with an empty string

for name in names:
	if len(name) > len(longestName):
		longestName = name

print("The longest name is: " + longestName)
# The longest name is laura
```

## Square map

Write a function called `squareMap` that takes in a list of numbers (integers or floats) and returns a list of the same length only each element has been squared.

Sample input/output:
```
>>> numbers = [1,2,3,5]
>>> squareMap(numbers)
[1, 4, 9, 25]
```

## Append Check

Write a function called `myAppend` that adds an element to a list provided that element is not already in the list. Remember that lists are passed by reference! The example below shows that the `myAppend` function does not actually return anything, it "mutates" (edits) the `animals` list.

Sample input/output:
```
>>> animals = ["cat", "dog", "elephant", "pig"]
>>> myAppend(animals, "dog")
>>> print(animals)
["cat", "dog", "elephant", "pig"]
>>> myAppend(animals, "zebra")
>>> print(animals)
["cat", "dog", "elephant", "pig", "zebra"]
```

*NOTE:* Try not to mutate lists with functions in the future. We are just trying to show you how lists work with functions.

## Pretty Print

The output of the inbuilt python `print` function doesn't look very good when printing a dictionary. Let's right a function called `pprint` to make the output look nicer.

```py
def pprint(aDict):
	# write your code inside this function
```

Sample input/output:
```
>>> D = {"name":"Alex", "age":27, "height":158}
>>> pprint(D)
{
	name:	Alex
	age:	27
	height:	158
}
```

*HINT:* Use the `D.items()` method and a for loop.


## Into the wild

Instead of going to work tomorrow you decide to go on an adventure. You have a number of items that you would like to take. However, you can only carry 7kg. Your job is to pack you bag with as many items as you can while ensuring that the weight of the backpack does not exceed 7kg. It is best to repesent the backpack as a dictionary:

```
> print(backpack)
{
	items:	["Toothbrush", "Sandwhich", "Bon Soy","Book on Python" ]
	weight:	2.750
}
```

Note this is not an optimisation problem. Put what ever you want in the backpack. Just make sure it is weighs less than 7kg.


Below is a list of your items that you could possibly take, where each item is represented as a dictionary:

```py
# copy and paste into your code if you like.
items = [
	{"name": "Toothbrush", "weight": 0.050},
	{"name": "Sandwhich", "weight": 0.100},
	{"name": "iPod", "weight": 0.250},
	{"name": "Tomahawk", "weight": 2.000},
	{"name": "Bon Soy", "weight": 1.000},
	{"name": "Sling Shot", "weight": 0.800},
	{"name": "Book on Python", "weight": 1.600},
	{"name": "Water", "weight": 1.800},
	{"name": "Tissues",  "weight": 0.150},
	{"name": "First Aid Kit", "weight": 0.750},
	{"name": "Flint", "weight": 1.075},
	{"name": "Magnifying Glass", "weight": 0.450}
]
```

*Bonus:* What is the best selection of items to maximise the number of items while keeping the weight below 7kg (i.e. make it an optimisation problem)?
