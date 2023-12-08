- Most popular open source container orchestration solution
- Provides Cluster Management
- Auto Scaling
- Service Discovery
- Load Balancer
- Self Healing
- Zero Downtime
- Auto Repair and Auto Upgrade
- Provides Pod and Cluster Autoscaling
- Enable Cloud Logging and Cloud Monitoring 
- Use Container-Optimized OS
- Provide support for Persistent disks and Local SSD

[[Google Kubernetes Engine/Basic Commands]]

- **Cluster**:
	- Master Node - Manages the Cluster
	- Worker Node - Run your workloads
- Master Node components
	- API Server
	- Scheduler
	- Control Manager
	- etcd - Distributed database storing the cluster state
- Worker Node components
	- Kubelet

[[Google Kubernetes Engine/Cluster Types]]

[[Google Kubernetes Engine/Pods]]

#### Kubernetes - Service
- Three types
	- Cluster IP - Exposes Service on a cluster-internal IP
		- When microservices only to be available inside cluster (intra cluster communication)
	- Load Balancer - Exposes Service externally using a cloud provider's load balancer
		- When want to create Load Balancer for each microservice
	- Node Port - Exposes Service on each Node IP at a static port
		- When you do not want to create an external Load Balancer for each microservice

#### Container Registry
- Fully managed container registry 
- Can be integrated to CI/CD tools to publish images to registry
- Analyze for vulnerabilities and enforce policies

```[!Info]
- Replicate master nodes across multiple zones for high availability
- Creating Docker Image for microservices
	- Build Image
	- Test it locally
	- Push it to Container Repository
- Supports Stateful deployments like Kafka, Redis, ZooKeeper
- Create a Pod for each node to store log collection or monitoring
	- DaemonSet (for background services)
- Integrates with Cloud Monitoring and Cloud Logging (Enabled by default)
```

[[Google Kubernetes Engine/Scenarios]]