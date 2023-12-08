- After updating instance template, you can trigger roll out of the new template using update-instances, recreate-instances or rolling-action start-update commands

```shell
gcloud compute instance-groups managed rolling-action [ restart | replace | rolling-action start-update [ --canary-version=v2-template,target-size=10% ] ]
```