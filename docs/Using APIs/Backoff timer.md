## Backoff timer

## General

Backoff timers are created by using these three parameters:
connection timeout, initial wait time, and wait rest time.

Start by using the initial wait time and double it after each timeout until it reaches wait reset time when it's reset back to the initial value.

Is important to think about which type of API call you using also because if you use a POST request and retry too much time it's a risk that you will create multiple entries instead of one. So in that case add a check to make sure that the object doesn't exist before testing again. 
