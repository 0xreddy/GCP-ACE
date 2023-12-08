- Simplest way to deploy and scale your applications
	- Provides end-to-end application management
- Supports Go, Java, .NET, Node.js, PHP, Python, Ruby
	- use custom runtime and write code in any language
- Pay for resources provisioned
- Features
	- Automatic load balancing and Auto scaling
	- Application versioning
	- Traffic splitting
	- Managed platform updates and Application health monitoring
- Lesser responsibility
- Lower flexibility

- Provides two different environments
	- **Standard** - Applications run in language specific sandboxes
		- Complete isolation
		- V1: Java, Python, PHP, Go
			- Only for Python and PHP restriction in network access
		- V2: Java, Python, PHP, Node.js, Ruby, Go
	- **Flexible** - Application instances run within Docker containers
		- Make use of Compute Engine VM
		- Support any runtime
		- Provide access to background processes and local disks

[[Google App Engine/Application Component Hierarchy]]

[[Google App Engine/ Environment Comparision]]

[[Google App Engine/Basic Commands]]

[[Google App Engine/Understanding App.yaml]]

[[Google App Engine/ Request Routing]]

[[Google App Engine/Deploying new versions without Downtime]]

[[Google App Engine/Splitting traffic]]

[[Google App Engine/App Engine Instances]]

[[Google App Engine/App Engine Services]]

[[Google App Engine/Cron Jobs]]

[[Google App Engine/Other yaml files]]

#### Things to Remember
 - App Engine is Regional
- Good option for simple microservices
	- Use Standard v2 when you are using supported languages
	- Use Flexible if you are building containerized apps
- At least one container is always running when using Flexible
	- Go for Standard if you want to be able to scale down the number of instances to zero when there is NO load
- Use combination of resident and dynamic instances
	- Resident Instances: Run continuously
	- Dynamic instances: Added based on load
		- Use all dynamic if you are cost sensitive

[[Google App Engine/Scenarios]]