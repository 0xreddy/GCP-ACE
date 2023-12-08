- Your own isolated network in GCP cloud
- Control all the traffic 
- (Best Practice) Create all your GCP resources within a VPC
- VPC is a global resource & contains subnets in one or more region

#### Need for VPC Subnets
- Different types of resources are created on cloud
	- Each type of resource has its own access needs
	- Load Balancers are accessible from internet
	- Databases or VM instance should NOT be accessible from internet
- Create subnets to separate public resources from private resources
- To distribute resources across multiple regions for high availability

### Firewall Rules
- Stateful
- Priority assigned (0-65535), 0 being the highest priority
- Default implied rule with lowest priority (65535)
	- Allow all egress
	- Deny all ingress
	- Default rules can't be deleted
	- Can override with high priority
- Ingress Rule: Incoming traffic from outside to GCP targets
- Egress Rule: Outgoing traffic to destination from GCP targets
- Along with each rule, we can also define
	- Priority
	- Action on match
	- Protocol
	- Port
	- Enforcement status

### Shared VPC
- Allows VPC network to be shared between projects in same organization
- Created at organization or shared folder level
- Shared VPC contains one host project and multiple service projects:
	- Host Project - Contains shared VP network
	- Service Projects - Attached to host projects
- Network administrators responsible for Host projects and Resource users use Service Project

### VPC Peering
- Networks in same project, different projects and across projects in different organizations can be peered
- All communication happens using internal IP addresses
	- Highly efficient
	- Highly secure
	- No data transfer charges
- Admin of one VPC do not get the role automatically in a peered network

### Hybrid Cloud
#### Cloud VPN
- Connect on-premise network to the GCP network
	- Using IPSec VPN Tunnel
- Two types
	- HA VPN
	- Classic VPN
#### Cloud Interconnect
- High speed physical connection between on-premise and VPC networks
- Data exchange happens through a private network
	- Reduce egress costs
#### Direct Peering
- Connect customer network to google network using network
- Not a GCP Service
- NOT RECOMMENDED
