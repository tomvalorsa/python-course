# Session 6 Problems

In session 6 we learnt about the following:

1. Datetime
2. Scheduling tasks
3. Launching Programs
4. Interfacing with Excel

Recall from session 4:

1. Reading, editing and writing text and csv files
2. Regular expressions

## Some theory to get us going...



## Houston, we have a problem...

The NASA employee who was supposed to read the countdown for today's space shuttle launch has woken up with a sore throat.
You have offered to use your python skills to write a program that will count down the last 20 seconds before liftoff.

It is important that the countdown announce each stage of the launch as it occurs:

16 seconds: Launch pad sound suppression system activated  
10 seconds: Main engine hydrogen burnoff system activated  
7 seconds: Main engine start  
1 seconds: Solid booster ignition  
0 seconds: Exact time (HH:MM:SS DD/MM/YYYY) of liftoff

A sample output is shown below:

```
>>> countdown(20)
Countdown started, T-minus 20
... 19
... 18
... 17
... 16 Launch pad sound suppression system activated
... 15
... 14
... 13
... 12
... 11
... 10 Main engine hydrogen burnoff system activated
... 9
... 8
... 7 Main engine start
... 6
... 5
... 4
... 3
... 2
... 1 Solid booster ignition
... 0
... Liftoff at 10:31:29 19/08/2016
```
