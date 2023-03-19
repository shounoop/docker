# docker push

The docker push command is used to upload a Docker image to a registry. You need to first tag the image with the name of the registry before you can push it.

For example, to tag an image with the name myregistry/myimage:latest, you can use the following command:

```cmd
docker tag myimage:latest myregistry/myimage:latest
```

Then, you can push the image to the registry using the following command:

```cmd
docker push myregistry/myimage:latest
```
