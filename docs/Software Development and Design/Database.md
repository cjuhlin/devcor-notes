\#database

# Database

## [ACID](https://en.wikipedia.org/wiki/ACID)

### Atomicity

All operation in the transaction must succeed otherwise it will rollback

### Consistency

Transaction result in valid state of the database , all validation and constraints are met. 

### Isolation

Transaction do not contend with one other. The transactions runs sequentially. 

### Durability

The result of transaction is permanent even in the presence of failures. 

## [Base](https://en.wikipedia.org/wiki/Eventual_consistency)

Is variant to ACID

### Basically availble

Reading and writing operations are available as much as possible (using all nodes of a database cluster), but might not be consistent (the write might not persist after conflicts are reconciled, the read might not get the latest write)

### Soft state

Without consistency guarantees, after some amount of time, we only have some probability of knowing the state, since it might not yet have converged

### Eventual consistency

If we execute some writes and then the system functions long enough, we can know the state of the data; any further reads of that data item will return the same value

## CAP

Model used for distributed database when is stored on multiple nodes. Only two of this three can be true at the same time. 

### Consistency

Every read receives the most recent write or error

### Availability

Every request receives a (non error) response, without guarantee that it contains the most recent write. 

### Partition tolerance

The database continues to operate even if an arbitrary number of messages were dropped by the network between nodes. 

### Conslusion

When a network fails the database becomes partitioned(out of sync with each other), and can it can do one of the following:

Ensure consistency and decrease availability by canceling the operation.

Ensure availability but risk inconsistency by proceeding the operation. 

\#needtofix

````
	Rewrite above with my own words. 
````

## Different type of database

### Relational database

Use [\#cap](Database.md#cap) (without p) and  [\#acid](Database.md#acid-https-en-wikipedia-org-wiki-acid).

#### When

* Best for structed data and querying structed data

### Document oriented database

#### When

### Serialize database

#### When

### Graph database

### Column oriented database

### Key oriented database

example mongodb

### Time-Series database

#### When

Best suited when handling data that comes with dates/time like logs. Using with telemetry information. Popular to use when building dashboards. 

\#needtofix 

````
	More example and why
````
