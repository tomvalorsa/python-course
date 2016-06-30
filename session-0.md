# Session 0 Problems

In Session 0 we:

1. Installed Python
2. Learned expressions and operators
3. Basic data types: integers, floating-point numbers and strings
4. Variables and statements

Work through the problems below at your own pace, do not hesitate to ask questions!

## A little theory
Which of the following are operators, and which are values?
```py
*
'hello'
-88.8
-
/
+
5
```

Why does this expression cause an error? How can you fix it?

```py
'I have eaten ' + 99 + ' burritos.'
```

## Computers love arithmetic
Write a script that prompts the user for two numbers, multiplies the numbers together and prints the result to the console.

```py
# To prompt the user to enter a value
my_string = input("Message to the user")
```

## Division
What is 17 divided by 3?
How many times does 3 divide into 7?

## Rounding numbers
Write a script that prompts the user for a floating point number and the number of decimal places to round the number, print the rounded number to the console. Python has a tool for doing this: `round()`.

Sample input/output:
```
> Enter a floating point number: 2.0453687
> How many decimal places would you like: 3
> The rounded number is: 2.045
```

## Greetings
Write a script that prompts the user for their full name, then print a message to the console. A sample is shown below (Google "python string split" if you get stuck).
What is your full name:
Hello Smith, Alex.


## Chasing outstanding debts
On the Yammer page you will find a csv file of project debts (it is not real data). A csv file looks likes an excel file, but it is actually just simple text separated by commas (hence comma separated values - csv). Your task is to find the sum of all the debts listed in the csv file.
Below is a sample of what is looks like:

|Job Number|Debt|
|-----|------|
|243156|1235.63|
|236412|2356.21|
|315224|23.01|

What would the instructions look like to do this by hand? Surprisingly, the instructions for the computer are quite similar.

Below is some python code that you can copy and paste into your script to read the csv line by line.

```py
import csv
with open("debts.csv") as csvfile:
  csvData = csv.DictReader(csvfile)
  for row in csvData:
    jobNumber = row['Job Number']
    debt = row['Debt']
    # Replace the code below with your magic
    print(jobNumber, debt)
```