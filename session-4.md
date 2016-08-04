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

file = open("example.txt", "w")
file.write("To write or not to write\nthat is the question!\n")
file.close()


file = open("example.txt", "r")

---> your code here


file.close()


Output
> Line 0 word count: 6
> Line 1 word count: 4

```

