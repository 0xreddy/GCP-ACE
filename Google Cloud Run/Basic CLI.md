```shell
# Deploy new container
gcloud run deploy SERVICE_NAME --image IMAGE_URL

# List available revisions
gcloud run revisions list

# Adjust traffic assignments
gcloud run services update-traffic myservice --to-revisions=v2=10,v1=90
```

