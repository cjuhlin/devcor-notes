\#rate-limit #ddos 

# Rate-limit

## Types of rate-limit

### REST API-calls

Return [HTTP code 429](..\Using%20APIs\HTTP%20Codes.md#4xx-429) when the end-user/client is making too many requests to let them know that the resource is busy right now. 

### Network traffic

Is important to have a rate-limit so it can lower the burden for network devices and servers during DDoS attacks. 

### User interaction

Stop brute-force attacks, example limit login attempts to three in an hour so they can't use brute-force attacks to figure out the password.

### Data protection

Do not allow frequent calls to extract data, so it's harder to use web-scrapping. 
