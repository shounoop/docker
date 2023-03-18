# docker run

The docker run command is used to run a Docker container from a Docker image. You can specify the image name and any additional options you want to use with the container.

For example, to run a container from the official Nginx image in detached mode (-d) and map the container port 80 to the host port 80 (-p 80:80), you can use the following command:

```cmd
docker run -d -p 80:80 nginx
```

Another example:
```cmd
docker run -it -p 8080:80 nginx
```

Naming container: 
```cmd
docker run -it -p 8080:80 --name mynginx nginx
```
