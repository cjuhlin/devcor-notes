\#latency

## Latency

To reduce latency you can use [load balancer](Load%20balancer.md) and do stuff on the client-side instead of the server. Like, generate the frontend on the client instead of everything on the server-side. Then let the backend just serve the static files. Then the client can use [API](..\Using%20APIs\using_api.md) to make a call to the backend to execute application logic on the frontend. 

````
(* In the above text we are talking about web applications. 
````

## Different types of latency

### Application latency

Latency is caused by the application. It can be minimized if you try to optimize your code where bottlenecks are occurring example functions that take a long time to perform a database query or calculation of something. If you using a language that compiles you can try to optimize the compiler to see if it helps. 

### OS and TCP stack latency

Latency that occurs in the OS when processing the request. 
Use an OS that reduces the latency to improve the latency. 

### NIC latency

How long time a packet spends in the interface queue and put into physical wiring for transferring. So choose a network card and speed that are necessary for the application to perform as it should. 

### Cable latency

Depending on what kind of cable and distance is used between the server and the client, it can create extra latency.

### Port to Port Latency

The network devices the packet is going through, if possible you can use better hardware to make the latency go down or make sure is going through so few network devices as possible between the server and the client. 

## Application optimization

There is some stuff you can do to optimize the application to reduce the latency, such as: 

### Content delivery network or local cache

It will reduce the latency for the end-user if there are different content delivery networks in different regions so the user will connect to the closest server that provides the same content. 

### Resource

#### Loading

Use [pagination](Pagination.md) so it will make smaller calls so you don't need to get all the data at the same time it will speed up everything and also use [lazy loading](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading).
