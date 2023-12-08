```yaml
runtime: python39 # The version 3.9 is written as 39
api_version: 1
service: service-name

inbound_services:
- warmup

env_variables:
	ENV_VARIABLE: "value"

handlers:
- url: /
  script: home.app

automatic_scaling:
	target_cpu_utilization: 0.65
	min_instances: 5
	max_instances: 100
	max_concurrent_requests: 50
```
