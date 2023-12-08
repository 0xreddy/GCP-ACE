```shell
gcloud app deploy # To deploy 
gcloud app list # List all services
gcloud app browse # Displays current active version of service
gcloud app browse --version=v2 # Get link to access specific version of the service
gcloud app services set-traffic --splits=v2=.3,v1=.7 # Split traffic between different versions
gcloud app services set-traffic --splits=v2=.3,v1=.7 --split-by=random
```


```shell
gcloud app [browse | create | deploy | describe | open-console]
```

```shell
gcloud app logs list # To list logs
```

