##### Three Approaches:
- Routing with URLs
	- https://PROJECT_ID.REGION_ID.r.appspot.com (default service called)
	- https://SERVICE-dot-PROJECT_ID.REGION_ID.r.appspot.com (specific service)
	- https://VERSION-dot-SERVICE-dot-PROJECT_ID.REGION_ID.r.appspot.com (specific version of service)
- Routing with a dispatch file
	- Configure dispatch.yaml
- Routing with Cloud Balancing
	- Configure routes on Load Balancing instance