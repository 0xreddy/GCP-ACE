### Cloud Monitoring
- Tools to monitor your infrastructure
	- Measures key aspects of services
	- Create visualizations
	- Configure alerts
		- Defining Alerting policies

#### Workspace
- Needed to organize monitoring information
	- Allows you to see monitoring information from multiple projects

### Cloud Logging
- Real time log management and analysis tool
- Allows to store, search, analyze and alert on massive volume of data
- Exabyte scale, fully managed
- Ingest Log data from any source
- Features
	- Log Explorer
	- Log Dashboard
	- Log Metrics
	- Log Router
- Most GCP Managed services automatically send logs to Cloud Logging
- Ingest logs from GCE VMs
	- Install Logging Agent
- Ingest from on-premises
	- Use BindPlane tool from Blue Medora
	- Use Cloud Logging API
#### Audit and Security Logs
- Access Transparency Log: Captures Actions performed by GCP team on your content
	- Only for organizations with Gold support level & above
- Cloud Audit Logs: Answers who did what, when and where
	- Admin activity logs - API calls or other actions that modify the configuration of resources
	- Data Access logs - Reading configuration of resources 
	- System Event Audit logs - Google Cloud administrative actions
	- Policy Denied Audit logs - When user or service account is denied access

![[Pasted image 20231206201346.png]]

#### Controlling & Routing

![[Pasted image 20231206201518.png]]

- 2 types of Logs buckets
	- \_Required: Holds Admin activity, System Events & Access Transparency logs (retained 400 days)
		- ZERO charge
		- You cannot delete the bucket
		- You cannot change the retention period
	- \_Default: All the other logs (retained 30 days)
		- You are billed on Cloud Logging pricing
		- You cannot delete the bucket
			- But you can disable the \_Default log sink route to disable the ingestion
#### Export
- Ideally stored in Cloud Logging for limited period
	- For long term retention logs can be exported to
		- Cloud Storage bucket
		- Big Query dataset
		- Cloud Pub/Sub topic

![[Pasted image 20231206203114.png]]

### Cloud Trace
- Distributed tracing system for GCP
- Find out
	- How long does a service take to handle requests
	- What is the average latency of requests
	- How are we doing over time
- Supported for
	- Compute Engine, GKE, App Engine etc
- Client libraries available for
	- C#, Go, Java, Node.js, PHP, Python & Ruby

### Cloud Debugger
- Capture state of a running application
	- Take snapshots of variables  and call stack
	- Very lightweight 
	- No need to add logging statements
	- No need to redeploy

### Cloud Profiler
- Statistical, low-overhead profiler
	- Continuously gathers CPU and Memory from production systems
	- Connect profiling data with application source code
		- Easily identify performance bottlenecks
	- Two major components
		- Profiling agent
		- Profiler interface

### Error Reporting
- Real-time exception monitoring
	- Aggregates and displays error reported from cloud services
	- Centralized Error Management console
	- Use Firebase Crash  Reporting for errors from Android & iOS client applications
- Errors can be reported by
	- Sending them to Cloud Logging
	- By calling error Reporting API

### Cloud Operations Scenarios

![[Pasted image 20231206210508.png]]
