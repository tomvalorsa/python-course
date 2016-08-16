## Cheat Sheet

Here are some commands for your reference that you will encounter throughout the sessions

## Session 0 - Getting Started

__Assigning variables__

Remember starting variable names with numbers is not allowed

2var = 0 # invalid variable name :-1:

var2 = 0 # valid variable name   :+1:

```py
var_name = 0           # integer
var_name = 'a string'  # string
var_name = 2.3         # float

```
__Converting Types__

Remember to switch between types to perform operations

```py
>>>str(3)
'3'
>>>int('2')
2
>>>float('3.2')
3.2
```

__Order of Operation__
```py
>>> (3+2)*5     # remember BOMDAS?
25

```

## Session 1 - Basics Part A
__For loops__
```py
for  i in range(10): # loops over the set -> 0,1,2,...,9
	print(i)

```

__While loops__

```py
i = 0 
while i < 10:
	print(i)
	i = i+1  # alternatively short hand is i += 1

```


## Session 2 - Basics Part B
__Defining a function__

```py
def add(a, b):
	return a+b
```

## Session 3 - Data Structures
```py

```

## Session 4 - Reading/Writing Files

__Splitting a string__
```py
>>>split_string = 'hello i am a string'.split() # returns a list split by whitespace
>>>split_string
['hello', 'i', 'am', 'a', 'string']


>>>csv_string = '1,2,456,789,1566'.split(',') # returns a list split by ,
>>>csv_string
['1','2','456','789','1566'] # note that these are still strings not ints
# you can use map and list to convert the  list
>>>csv_ints = map(int,'1,2,3,4,5'.split(','))
>>>csv_ints
[1,2,456,789,1566]

```
__Opening a file__
```py
f = open('file.txt', 'r')    # read mode
f = open('file.txt', 'w')    # write mode
f = open('file.txt', 'a')    # append mode
```
__Reading a file__
```py
f = open('file.txt', 'r')    # read mode
lines  = f.readlines()       # returns a list of strings representing your lines in your file
for line in lines:           # iterate over each line in your list of lines
  print(line)                # print out each line to the shell
f.close()
```

__Writing a file__
```py
f = open('file.txt', 'w')    # read mode
f.write("To write or not to write\nthat is the question!\n")
f.close()
```
