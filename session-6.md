# Session 6 Problems

In session 6 we learnt about the following:

1. Datetime
2. Interfacing with Excel

Recall from session 4:

1. Reading, editing and writing text and csv files
2. Regular expressions

## Some theory to get us going...

The Unix time variable (timestamp) is based on the total seconds elapsed from the Unix Epoch (12 AM 1st January 1970 UTC).

```
>>> import time
>>> time.time()
1471568701.1974244
```
When we call ```time.time()``` we can assign it to a variable, eg ```time_now = time.time()``` and perform operations as usual - remember this operates in seconds.
```
>>> import time
>>> before = time.time()
>>> after = time.time()
>>> after - before
4.694000005722046
```
We can also call ```datetime.datetime.now()``` which will return a datetime object, which can then be formatted. 
```
>>> import datetime
>>> date_today = datetime.datetime.now()
>>> date_today
datetime.datetime(2016, 8, 22, 8, 46, 4, 937283)
>>> date_today.strftime('%d/%m/%Y')
'22/08/2016'
>>> date_today.strftime('%H:%M:%S')
'08:46:04'
>>> date_today.strftime('The date is %d/%m/%Y, the time is: %H:%M:%S')
'The date is 22/08/2016, the time is: 08:46:04'
```
We can advance or rewind a particular datetime by using ```datetime.timedelta()```.
```
>>> import datetime
>>> time_now = datetime.datetime.now()
>>> time_later = time_now + datetime.timedelta(days=10, hours=5, minutes=24, seconds=12)
>>> time_later.strftime('%H:%M:%S %d/%m/%Y')
'14:16:43 01/09/2016'
```

When we are running a program (for example a ```for``` loop), we can delay the program using the ```time.sleep()``` function:

```
>>> import time
>>> def wait_ten_seconds():
	    print('Waiting for 10 seconds')
	    time.sleep(10)
	    print('Finished!')
>>> wait_ten_seconds()
Waiting for 10 seconds
Finished!
```

## Hints and best practice

Often to cancel a running python script you can push CTRL-C.
Due to the nature of the time.sleep() function, it cannot be interrupted.

Instead of this:

```py
def delay_function(seconds):
  time.sleep(seconds)
  print('Delay complete')
```
try this:
```py
def delay_function(seconds):
  for i in range(seconds):
    time.sleep(1)
  print('Delay complete')
```

## Houston, we have a problem...

The NASA employee who was supposed to read the countdown for today's space shuttle launch has woken up with a sore throat.
You have offered to use your python skills to write a program that will count down the last 20 seconds before liftoff.

It is important that the countdown announce each stage of the launch as it occurs:

16 seconds: Launch pad sound suppression system activated  
10 seconds: Main engine hydrogen burnoff system activated  
7 seconds: Main engine start  
1 seconds: Solid booster ignition, booster-tower separation  
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
... 1 Solid booster ignition, booster-tower separation
... 0
... Liftoff at 10:31:29 19/08/2016
```

## Excel Problem
