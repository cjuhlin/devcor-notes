#resilence

# Resilence

## Types

### Parameters checking

Complete parameters checking in functions and objects to protect from broken and malicious calls. 

### Timeouts
Timeout should be trimmed so the request isn't taking a too long time but also allowing slower response for stuff that takes some longer time than other functions. 

### Asynchronous communications

Is used to decouple the sender from the receiver and prevent failure dues to failing/slow resources. 

### Fan out and use the quickest response

Used to send many requests and the first, quickest reply is used. The other request is discarded, this is wasteful of resources. 

### Fail fast

If the application knows that something will fail, it should fail fast so it will not use resources for no reason. 

### Circuit breaker

Is a variant of [[#Fail fast|fail fast]] . If a call fails multiple times a circuit breaker will take that resource offline and return an error on the next attempt. 

### Retries

Used to repeat the same operation multiple times and hope that it will work around temporary network problems or system problems. Important to know is that if the operation that you are trying to retry is resourced heavy it will just make everything worst for the system that is going to process the operation. 

### Fallback mechanism

Fallback to a default value or cached value if possible. Sometimes this is not possible because of the nature of the requested data example if a credit card is valid or not. 


