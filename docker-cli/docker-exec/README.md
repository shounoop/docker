# docker exec

The docker exec command is used to execute a command inside a running Docker container. You need to specify the container ID or name of the container you want to execute the command in, as well as the command you want to execute.

For example, to execute the ls command inside a container with ID CONTAINER_ID, you can use the following command:

```cmd
docker exec CONTAINER_ID ls
```

Another example:
```cmd
docker exec -it CONTAINER_ID bash
```
