## Backoff timer

## General

Backoff timer are created by using this three parameters:
connection timeout, initial wait time and wait rest time.

Start by using initial wait time and double it after each timeout until it reach wait reset time wen it's reset back to initial value.

Is important to think about which type of API call you do also, because if you using a POST request and retries many time it's risk that you will create multiple entries instead of one. So in that case add a check to make sure that the object doesn't exist before testing again. 
