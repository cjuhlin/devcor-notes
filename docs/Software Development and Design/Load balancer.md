#loadbalancer #lb
# Load balancer (LB)

A load balancer is a server that is before the application server. It makes it easier to manage application that is running on multiple instances instead of a single instance. You set the IP for accessing the application on the load balancer instead of the application server and let the load balance route the traffic to the right server. 

You can use something that calls global server load balancing if you have users all over the world. So if you deploy a load balancer in each region then you can configure it so that the user will connect to the LB with the lowest latency instead of getting a response from a server on the other side of the world. 

## Pros

* High availability and reliability 
	* Check servers healthy before routing the traffic to the server, so if a server is offline it will send it to another server that is online instead. 
* Reduced downtime
	*  A single server will not take down everything if something is wrong because of the above point. 
* [[Scalabilty]] / Flexibility
	* Easy to add more servers behind the LB to scale
* Efficiency 
	* Different types of load balancing, you can configure the LB to balance the traffic after how much traffic, response time, and more. 