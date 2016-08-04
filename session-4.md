# Session 4 Problems

In session 4 we learned how to read and write data from a file.

1. splitting strings
2. iterating over lines

## A little theory

 - What is a relative path relative to?
 - What does an absolute path start with?
 - What are the . and .. folders?
 - In C:\bacon\eggs\spam.txt, which part is the dir name, and which part is the base name?
 - What are the three “mode” arguments that can be passed to the open() function?
 - What happens if an existing file is opened in write mode?
 - What is the difference between the read() and readlines() methods?

## Evaluating lines

Below is a snippet that will open and close a file, can you write some code that will eveluate the word count of line of text in example.txt
print it to the screen?

```py

f = open("example.txt", "w")
f.write("To write or not to write\nthat is the question!\n")
f.close()

f = open("example.txt", "r")

... your code here

f.close()


Example Output

> Line 0 word count: 6
> Line 1 word count: 4

```

## Tails

You land your dream job at the bureau of meteorology and the weather is your oyster. Your first job is to check the logs of weather stations around your area and make that the data is being recorded correctly. Using your wealth of programming knowledge you devise a plan to write a python program that will do you work for you. 

The program reads the last n recordings of the logs will do you work for you while you kick back and daydream what an aurora borealis tornado might look like.

Pro tips
 - Save the folder full of weather files from github to your desktop
 - Save you file in a place where you can access these files 'relatively' easily

```py
# Create a list of logs
logs = ...your code here

for log in logs:
	f = open(log, "r")
	...your code here. get the last n recrodings from the file. 
	Think about how would you check if the recordings are likely to be valid?
	f.close()

Example Outputs

> Weather Station x recordings appear valid
> Weather Station y recordings seem fishy... take a better look

```
