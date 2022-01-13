\#rate-limit #ddos 

# Rate-limit

## Types of rate-limit

### REST API-calls

Return [HTTP code 429](..\Using%20APIs\HTTP%20Codes.md#4xx-429) when the end-user/client is making to much request to let they know that the resource is busy right now. 

### Network traffic

Is important to have rate-limit so it can lower the burden for network devices and servers during DDoS attacks. 

### User interaction

Stop brute-force attacks , example limit login attempts to three in a hour so they can't use brute-force attacks to figure out the password.

### Data protection

Do not allow frequents calls to exctract data , so it's harder to use web-scrapping. 
