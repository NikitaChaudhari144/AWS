1. Global Table
    A global table in DynamoDB is a fully replicated, multi-region, multi-master database that provides high availability and low latency for globally distributed applications. It automatically replicates data across multiple AWS regions.
    Problems with Global Tables:
    •	Consistency Issues: Due to eventual consistency across regions, conflicts can arise.
    •	Cost: Higher cost due to data transfer and storage in multiple regions.
    •	Latency: Writes in one region need to be propagated to other regions, which can cause latency.
    •	Complexity: Management and troubleshooting become more complex with multi-region setups.
    Differences from Normal Table:
    •	Replication: Global tables replicate data across multiple regions, whereas normal tables are confined to a single region.
    •	Availability: Global tables offer higher availability across multiple regions compared to normal tables.


2. Consistency Models
    Strong Consistency:
    •	Definition: Ensures that a read always returns the most recent write.
    •	Example: Reading data immediately after a write operation will reflect the new data.
    Eventual Consistency:
    •	Definition: Ensures that, over time, all reads will eventually return the most recent write, but not necessarily immediately.
    •	Example: Reading data after a write operation may not immediately reflect the new data, but will eventually do so.
    Transactional Consistency:
    •	Definition: Ensures atomic, consistent, isolated, and durable (ACID) transactions.
    •	Example: Multiple operations within a transaction are either all completed successfully or none are.


3. Difference in Local Index and Global Index
    Local Secondary Index (LSI):
    •	Scope: Limited to a single partition key.
    •	Definition: An index that uses the same partition key as the table but a different sort key.
    •	Use Case: Querying data using alternative sort keys.
    Global Secondary Index (GSI):
    •	Scope: Can span across all partition keys.
    •	Definition: An index that uses a different partition key and sort key from the table.
    •	Use Case: Querying data using different partition and sort keys than those of the table.


4. What is DynamoDB?
    DynamoDB is a fully managed NoSQL database service provided by AWS that offers fast and predictable performance with seamless scalability. It is designed to handle large amounts of data and support high-traffic applications.


5. Other NoSQL Databases
    •	MongoDB: Document-oriented database.
    •	Cassandra: Column-family store.
    •	Redis: In-memory key-value store.
    •	Couchbase: Document-oriented database with strong consistency.


6. Advantages of Using DynamoDB
    •	Scalability: Automatically scales throughput capacity.
    •	Performance: Provides low latency at any scale.
    •	Fully Managed: Reduces the operational burden.
    •	Global Tables: Provides high availability and multi-region replication.
    •	Built-in Security: Encryption at rest and in transit.
    •	Event-Driven: Supports DynamoDB Streams for real-time processing.
    Why Choose It and When:
    •	High Traffic Applications: When you need a database that can handle millions of requests per second.
    •	Scalability: When you need to scale seamlessly with demand.
    •	Flexibility: When you need a flexible schema.


7. When DynamoDB is Not a Right Fit
    •	Complex Queries: When you need complex queries involving joins or multiple table operations.
    •	Transactions: When ACID transactions are a must for every operation.
    •	Relational Data: When data is highly relational and fits better into a relational database.


8. Use Cases of DynamoDB
    •	Gaming: Real-time game state and player data.
    •	IoT: Storing and querying device data.
    •	E-commerce: Shopping cart and user session data.
    •	Ad Tech: Storing user profiles and serving real-time ads.


9. Partition Key and Sort KeyS
    •	Partition Key: The primary key used to distribute data across partitions.
    •	Sort Key: An additional key used to sort data within the same partition.


10. DynamoDB Streams
    •	Definition: Captures a time-ordered sequence of item-level changes in a table.
    •	Why Used: For real-time processing and replication.
    •	Where Used: Triggering AWS Lambda functions, data replication, and auditing.


11. DynamoDB Capacity Charges
    •	Provisioned Capacity: Charges are based on the amount of read and write throughput you provision.
    •	On-Demand Capacity: Charges are based on the actual reads and writes you perform.


12. Data Encryption in DynamoDB
    •	Encryption at Rest: Uses AWS Key Management Service (KMS) to encrypt data stored on disk.
    •	Encryption in Transit: Uses TLS/SSL to encrypt data in transit.


13. DynamoDB Accelerator (DAX)
    •	Definition: An in-memory caching service for DynamoDB.
    •	Purpose: Provides fast in-memory performance for read-heavy and bursty workloads.
    •	Benefits: Reduces latency from milliseconds to microseconds.
