# SYSTEM DESIGN

System design is the process of defining the architecture, components, modules, interfaces, and data for a system to satisfy specified requirements. It’s basically how you plan and organize a complex system to work efficiently and reliably.

In system dsign we will be learning about RESOURSE avablities,how their resources work together and utilization and trades off.


IN SYSTEM DESIGN WE WILL BE LEARNING ABOUT-

- LOAD BALANCING
- CAP THEOREM
- SQL AND NOSQL
- CONSISTANT HACKING
- QUEUES
- CASHING
- REPLICATION
- INDEXES 
- PROXIES
- DATA PARTITINING



# LOAD BALANCING
- For better scabality and data retundency we us 3 load balancers
- we use 1 load balancer bw client\user and web server
- next between web server and app server(internl platform)
- and last bw app server\intrnal platforn and database

There are basically 2 type of load balacers 
- *Hardware load balancer
- *Software load balancer

## HARDWARE LOAD BALANCER
- THIS LOAD BALANCER IS EXPENSIVE AND GIVES US HIGH PRFORMANCE THAN SOFTWARE LOAD BALANCER
- MANY COMPANIES AVOID SUCH LOAD BALANCER AS IT IS A DEDICATED HARDWARE AND UTILISE A LOT OF PACE AND POWER
- WHEN THE CPMANIES BECAME VERY LARGE AND SOFTWARE LBs ARE NOT ABLE TO HANDLE THE LOAD THEN HARD WARE LBs ARE USED.


## SOFTWARE LOAD BALANCER
- THERE IS NO COST OF PURHASING DEDICATE SOFTWARE AND IS EASY TO USE AS IT IS A SIMPLE SOFTWARE TO INSTALL
- NEW STARTUPS OR COMPANIES PREFER TO USE IT

# CAP THEREM


## C: Consistency
Every read receives the most recent write or an error. In other words, all nodes see the same data at the same time.

## A: Availability
Every request receives a response (success or failure), without guarantee that it contains the most recent write.

## P: Partition Tolerance
The system continues to operate despite network partitions (communication breakdowns between nodes).
- IF ANY PART OF SYSTM FAILS OR RAISE AND ERROR PRTITION TOLLERANCE HELPS TO KEPP ON RUNNING OTHER FUNCTIONS WITHIUTH CLOSING FULL SYSTEM.


### CAP theorem says you can only have two out of these three guarantees at the same time in a distributed system — never all three.
When a network partition (communication break) happens, servers can’t talk to each other.

To be consistent, servers must agree on the latest data, so some may reject requests, reducing availability.

To be available, servers respond anyway, even if they don’t have the latest data, reducing consistency.

So during a partition, you must choose either consistency or availability, but not both.



# SQL and NOSQL
## SQL
SQL stands for Structured Query Language.

It refers to relational databases that store data in tables with rows and columns.

Uses fixed schemas to define the structure of data.

Examples: MySQL, PostgreSQL, Oracle, SQL Server.

## NOSQL
NoSQL means “Not Only SQL” or non-relational databases.

Stores data in flexible formats like key-value pairs, documents, graphs, or wide-columns.

Usually schema-less or has dynamic schemas.

Examples: MongoDB (document), Redis (key-value)

### DIFFERENCES
| Aspect         | SQL                              | NoSQL                                              |
| -------------- | -------------------------------- | -------------------------------------------------- |
| Data Model     | Relational (tables)              | Non-relational (documents, key-value, graph, etc.) |
| Schema         | Fixed schema                     | Flexible or dynamic schema                         |
| Query Language | SQL                              | Varies by database (e.g., JSON queries, APIs)      |
| Scalability    | Vertical scaling (scale-up)      | Horizontal scaling (scale-out)                     |
| Transactions   | Strong ACID compliance           | Often eventual consistency, some support ACID      |
| Use Cases      | Complex queries, structured data | Big data, real-time apps, flexible data            |

