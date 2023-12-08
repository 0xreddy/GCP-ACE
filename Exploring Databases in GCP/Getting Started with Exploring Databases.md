### Cloud SQL
- Fully managed Relational Database service
	- Configure your needs and do not worry about managing the database
	- Supports MySQL, PostgreSQL, and SQL Server
	- Regional Service providing High Availability (99.95%)
- To migrate local MySQL, PostgreSQL and SQL Server databases
- To reduce your maintenance cost for a simple relational database
- Use Cloud Spanner if
	- huge volumes of relational data
	- infinite scaling
	- higher availability

```shell
gcloud sql connect <instance-name> --user=root --quiet
```
#### Features
- Automatic encryption, maintenance and updates
- High availability and failover
- Read replicas for read workloads
- Automatic storage increase without downtime
- Point-in-time recovery
- Backups
- Support migration from other sources
- Export export data from UI or gcloud with formats

### Cloud Spanner
- Fully managed, mission critical, relational, globally distributed database with VERY HA (99.999)
- Scales horizontally for reads and writes
- Expensive: Pay for nodes & storage
- Data Export: Use Cloud Console to export data

### Cloud Datastore and Firestore
- Datastore - Highly scalable NoSQL Document Database
	- Automatically scales and partitions data as it grows
	- Recommended for up to a few TBs of data
	- Support Transactions, Indexes and SQL like queries
	- For cases needing flexible schema with transactions
	- Only export data from gcloud
- Firestore - Datastore++
	- Optimized for multi device access
	- Offline mode and data synchronization across multiple devices
	- Provides client side libraries
	- Offers Datastore and Native modes

### Cloud BigTable
- Petabyte scale, wide column NoSQL DB (HBase API compatible)
	- Single row transactions
- Not serverless
- Cannot export data using cloud console or gcloud
- "cbt" cli tool to interact in gcloud console

### Memorystore
- In-memory datastore service - Reduce access time
- Fully managed
- Support Redis(low latency) and Memcached

### BigQuery
- Exabyte scale modern Datawarehousing solution from GCP
	- Relational database
	- Traditional(Storage + Compute) + Modern (Realtime + Serverless)
- Load from a variety of sources
- Export to Cloud Storage(long term storage) & Data Studio(visualization)
- Automatically expire data
- Query external data sources without storing data in BigQuery
	- Cloud Storage, Cloud SQL, BigTable, Google Drive
- Access using
	- Cloud Console
	- bq command-line tool
	- Rest API
	- Hbase API based libraries
- Very expensive
- **BEST PRACTICE** - Estimate BigQuery queries before running
	- Use UI/bq - Get scanned data volume
	- Use Pricing Calculator - find price for 1MB data. Calculate cost

### Cloud SQL
```shell
gcloud sql instances create | clone | delete | describe | path

gcloud sql  databases create | list | delete | describe | path

gcloud sql connect INSTANCE [--database=DATABASE --user=root]

gcloud sql backups create | describe | list
```

```shell
bq shell 

bq query 'QUERY_STRING'

bq extract
bq load
```

```shell
cbt createinstance | createcluster | listinstances | listclusters | ls | createtable | deleteinstance
```

### Relational Database - Import and Export Support
![[Pasted image 20231127102401.png]]

### NoSQL Databases - Import and Export Support
![[Pasted image 20231127103031.png]]

> [!REMINDER]
> ![[Pasted image 20231127103204.png]]

