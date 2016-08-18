# Session 5 Problems

In session 5 we learned:

1. Errors and Exceptions
2. Debugging and testing using logging

Take the opportunity to practice everything that you have learned in the course so far. Use the concepts taught in session 5 to help debug and test your programs.

## Password Generator

The first tool that hackers use to crack passwords is social engineering. Social engineering essentially involves stalking you on social media, email etc and guess your password from birthdays and family names. Lets write a python program that generates a password on request that cannot be subject to social engineering hacking.

First lets build a completely random password. Write a function called `generate_password` that generates a password of 12 characters. The code below will help you get started.

```py
import string
import random

def generate_password():
	possible_chars = string.ascii_letters + string.digits # what is string.ascii_letters and string.digits ?
	password = ''
	# write your python code here
	# use a for loop and look into (google) python's random.choice module

```

Sample input/output
```
>>> password = generate_password()
>>> print(password)
d9WDf9F35fsg
```

This definitely produces a secure password. There are actually 62^12 different combinations, thats 3,226,266,762,397,899,821,056 possible passwords!!!

## Human Password Generator

Who can remember a password like the ones generated above. Lets build another password generator. This time lets combine two random words and three numbers. It will be much easier to remember.

In the [resources](https://github.com/tomvalorsa/python-course/tree/master/resources) folder in this github page you will find a very long list of words to choose from. Write a function called `generate_password2` that returns a random password as described above. This problem will require some careful planning. Try to break the problem down into logical sub-problems and build functions. Here is a few likely sub-problems to get you started:

1. read the words.txt file
2. build a `list` of words from the file
3. randomly select two words from the list and three numbers
4. combine words and numbers into one string and return to the user

Sample input/output
```
>>> password = generate_password2()
>>> print(password)
bakedfool112
>>> password2 = generate_password2()
>>> print(password2)
blackmandarin685
```

## Session Attendance

We would like you to investigate attendance in the python course. In the [resources](https://github.com/tomvalorsa/python-course/tree/master/resources) folder in this gitbhub page there is a csv file with recorded attendance for sessions 0-8. We would like to know two things from the data set:

1. What was the attendance for each session (to determine popular sessions)
2. What was the attendance for each person (to determine if people are consistently attending sessions)

Again, plan carefully for this problem. Think about the steps to solve the problem and break it down into functions.

A sample of the output of the analysis is shown below.
```
>>> print(session_attendance)
------------------------------
Attendance for each sessions:
------------------------------
Session 0: 41
Session 1: 45
Session 2: 38
Session 3: 23
Session 4: 49
Session 5: 28
Session 6: 37
Session 7: 42
Session 8: 39
------------------------------
Attendance consistency
------------------------------
8 Sessions: 5 people
7 Sessions: 12 people
6 Sessions: 35 people
5 Sessions: 42 people
4 Sessions: 38 people
3 Sessions: 26 people
2 Sessions: 16 people
1 Sessions: 4 people
0 Sessions: 0 people
------------------------------
```
## Common Words

Have you ever listened to a politician give a speech?
In the [resources](https://github.com/tomvalorsa/python-course/tree/master/resources) folder there is a .txt copy of the 2016 budget speech delivered by Honourable Scott Morrison MP, Treasurer of the Commonwealth of Australia - download this file and save it in your working directory.

We would like to find out a few things from the speech:

1. What were the 20 most frequently used words?
2. How could you make these results more interesting/relevant? (hint: remove words with < 3 letters)

A simple approach we would recommend is to use a dictionary to store words and their corresponding frequencies.
You will need to extract each word from the speech individually, remembering that 'Tax' is not the same as 'tax' (hint: or 'tax,').

How would you extract each word from the following sentence: "Tax, tax and more tax."

A generic code snippet that prints the first ten key-value pairs from a dictionary, from largest to smallest:

```
>>> animal_frequency={'frog':5, 'antelope':2, 'toucan':3}
>>> for word, frequency in letter_frequency.items():
		print(word, frequency)
toucan 3
antelope 2
frog 5
```

This is not in any particular order. How would you sort these values by their frequencies?

A sample output is shown below:

```
Word: 'the', frequency: 198 
Word: 'and', frequency: 164
Word: 'will', frequency: 80
Word: 'for', frequency: 69
Word: 'tax', frequency: 65
Word: 'our', frequency: 53
Word: 'this', frequency: 46
Word: 'are', frequency: 38
Word: 'that', frequency: 37
Word: 'their', frequency: 36
Word: 'jobs', frequency: 36
Word: 'new', frequency: 30
```
