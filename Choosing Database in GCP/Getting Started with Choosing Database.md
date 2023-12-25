#### Databases Primer
- Database provide organized and persistent storage for your data
- To choose between different database types. we would need to understand
	- Availability
	- Durability
	- RTO
	- RPO
	- Consistency
	- Transactions and so on

#### Availability
- Percentage of time an application provides the operations expected of it
#### Durability
- How long lasting the data in database is

##### Increasing Availability and Durability of Databases
- Increasing Availability
	- Have multiple standbys available or distribution the database
- Increasing Durability
	- Multiple copies of data
- Replicating data

#### RTO and RPO
- Recovery Point Objective
- Recovery Time Objective
- Achieving minimum RTO and RPO is expensive, there will be tradeoffs
##### Failover Examples
![[Pasted image 20231124142013.png]]

#### Consistency
- Strong consistency - synchronous replication to all replicas
- Eventual Consistency - Asynchronous replication
- Read-after-Write consistency - inserts are immediately

#### Database Categories
- Relational, Document, Key Value, Graph, In Memory...
- Choosing type of database
	- fixed schema?
	- level of transaction properties do you need?
	- latency?
	- how many transactions?
	- how much data?

#### OLTP online transactions processing 

![[Pasted image 20231208220723.png]]

#### OLAP  Online Analytics processing 

![[Pasted image 20231208220757.png]]

#### NoSQL (Cloud Big Table vs Cloud Firestore)

![[Pasted image 20231208220842.png]]

![[Pasted image 20231208220906.png]]

#### In memory

![[Pasted image 20231208220926.png]]

#### Database - Summary
![[Pasted image 20231124144859.png]]

#### Database - Scenarios
![[Pasted image 20231124224333.png]]

