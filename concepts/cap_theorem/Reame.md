# The CAP Theorem

In any distributed syetm, you can y gurantee 2 of the 3:

* Consistency - Every read gets the latest write
* Availability - Every requuest receives a response
* Partition Tolerance - System continues despite failures

No sytem can have all 3 at the same time

Note: Since network partitions are unavoidable, especially at scale, real-world sytems must choose between Consistency and Availability during partition.

### CP (Consistency + Partition Tolerance)
* Prioritize data correctness over availability
* During partion, the system may reject requets to avoid inconsistent reads
* Example: HBase
* Usecase: Financial systems, banking apps, anywhere data integrity is critical

### AP (Availability + Partition Tolerance)
* Prioritizes system uptime over consistency
* System will return datle or eventually consistent data
* Example: DynamoDB, Cassandra
* Usecase: Social Meedia feeds, product catalog, DNS

### CA (Consistency + Availability) - The "Unicorn"
* Only possible if no network partitions ever occur - i.e in single node or tighly coupled systems
* In practice, not acchievable in distributed systems that need to tolerate network faults