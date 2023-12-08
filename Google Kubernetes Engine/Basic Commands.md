```shell
gcloud container clusters create # Create a cluster
gcloud container clusters get-credentials <cluster-name> --zone <zone-name> --project <project-name> # Fetching the credentials
kubectl create deployment <deployment-name> --image=<image-name> # Deploying microservices
kubectl get deployment # Get the deployments
kubectl expose deployment <deployment-name> --type=LoadBalancer --port=8080
kubectl get services # Get the services
kubectl scale deployment <deployment-name> --replicas=3 # Scaling the containers
gcloud container clusters resize <cluster-name> --node-pool <pool-name> --num-nodes=2 # Resize the node pool in the cluster

# Horizontal auto scaling
kubectl autoscale deployment <deployment-name> --max=4 --cpu-percent=70

# Auto scale cluster
gcloud container clusters update cluster-name --enable-autoscaling --min-nodes=1 --max-nodes=10

# Add some application configuration for your microservice
# Config Map
kubectl create configmap todo-web-application-config --from-literal=RDS_DB_NAME=todos

# Add password configuration for your microservice
kubectl create secret generic todo-web-application-secrets-l --from-literal=RDS_PASSWORD=dummytodos

kubectl delete service

gcloud container clusters delete
```

![[Pasted image 20231026221318.png]]