# docker ps

The docker ps command is used to list running Docker containers. You can specify any additional options you want to use with the command.

For example, to list all running containers along with their port mappings and container IDs, you can use the following command:

```cmd
docker ps -a --format "table {{.ID}}\t{{.Names}}\t{{.Ports}}"
```
