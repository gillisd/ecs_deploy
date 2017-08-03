# ECS Deploy
ECS Deploy is a simple script you can run to update your ECS task definition following the push of a new Docker image.
It works great a post-deploy script on your CI provider.

## Deploying

To execute a deployment:

```console
$ # Push a container to your docker registry
$ python deploy.py deploy --cluster=<cluster> --service=<service> --image=<image> --container=<container>
```

It will then update the image being used by that service's task. ECS will handle
updating the running containers.

Thank you github.com/alex