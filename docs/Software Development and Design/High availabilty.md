\#highavailabilty #availabilty 

# High availability

## Singel point of failure

It's important to build redundancy into the system so that if one part fails everything doesn't fail. 

## Reliable failover

When something fails it should switch over to a working instance instead of completely failing. 

## Detection of failures as they occur

Monitoring the system health so that the traffic doesn't go to a node that is down. One thing to use here is a [load balancer](Load%20balancer.md). But you should also have a monitoring system to get an alarm when something goes down or other issues with the node. 
