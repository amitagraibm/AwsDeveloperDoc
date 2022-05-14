EC2 = Elastic Cloud Compute
An EC2 instance is the basic unit of AWS infrastructure. Basically all of the other AWS services use EC2 under the hood.

Instance types

General purpose
Balanced compute, memory and networking resources
Use cases: web servers, code repos
Instance codes: A1, M4, M5, M5a, T2, T3, T3a

Compute optimized
High-performance processors
Use cases: scientific modeling, gaming servers, ad server engines
Instance codes: C4, C5, C5n

Memory optimized
For workloads that process large datasets in memory
Use cases: in-memory caches and databases, real-time analytics
Instance codes: R5, R5a, X1e, X1, z1d, High Memory

Accelerated optimized
Hardware co-processors
Use cases: machine learning, speech recognition, computational finance
Instance codes: F1, G3, P2, P3

Storage optimized
High read and write access to large data sets
Use cases: NoSQL and relational databases
Instance codes: D2, H1, I3, I3en

Placement groups

Cluster: instances clustered close together inside a single availability zone (AZ)
Partition: distributes clusters of instances across separate racks
Spread: each instance is on a separate rack, and can be in a separate AZs.

Instance profiles

IAM Policy -> IAM Role -> Instance Profile -> EC2 instance
Always avoid embedding your credentials in source code.
An Instance Profile holds a reference to a role. This allows the EC2 instance to access other AWS services, without needing your direct credentials.

User data and metadata
User data or UserData is a script that is run when an EC2 instance is launched.
Meta data about the instance can be seen at runtime by hitting a URL endpoint: http://169.254.169.254/latest/meta-data.
