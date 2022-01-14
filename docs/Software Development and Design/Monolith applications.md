\#monolith #single #application

# Monolith application

Monolith application is one single big application.  Everything is on one node, the whole application; the presentation, the logic, and the database interface.

Designed to do every step in the process without using external services.

## Pros

### Easier to deploy

Because everything is one single unit that is going to be installed on one node it makes it easier to deploy, just install it on the node with all the requirements, and is done. 

### Lower [Latency](Latency.md)

Because everything is on the same node everything takes less time for the application to communicate with everything internal. 

## Cons

### Too big

When the application is too big it will make it harder to manage. 

### Redeploy

Need to redeploy the whole thing when making small changes (single file application mostly)

### [Scaling](Scalabilty.md)

If some component in the application hugs up the resource it will be harder to deploy the application to multiple servers to scale. You will also need to deploy the whole application to the new nodes not only part of the application that is needed that extra resource. But if the application was broken into [microservices](Microservices.md) then you could just do [horizontally scaling](Scalabilty.md#scaling-horizontally) and deploy the microservice on the new nodes.

### Only one codebase

The whole application needs to be done in one language. So sometimes for a certain task that chosen language is maybe not best suited for the job example C++ maybe not be so great for web frontend but better for some backend stuff. 
