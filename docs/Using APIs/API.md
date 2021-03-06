\#api

## API

## General

Two types of API calls, synchronous and asynchronous. 

### Synchronous

The client makes a call and waits for a response before proceeding

### Asynchronous

The client make a call and the API response back that it received that call but not if it was successful or not, the client need to request that information later. 

### Retries

Use [backoff timer](Backoff%20timer.md) for making retries to an API. If you don't use the backoff timer and make retries all the time till it works it will make the server loads higher and worst-case DoS-attack without knowing that. In some case if the API have [rate-limit](..\Software%20Development%20and%20Design\rate-limit.md#rest-api-calls) it will response back with [HTTP 429 code](HTTP%20Codes.md#4xx-429) .

Sometimes some APIs use "X-Rate-Limit-Remaining" and "X-Rate-Limit-Reset" in a response header to inform you about the status of retries. 

In [Webex](..\Cisco%20Platforms\Webex.md) API they are using the "Retry-After" header in the response when getting [HTTP code 429](HTTP%20Codes.md#429) to inform you about when you can try next time. 
