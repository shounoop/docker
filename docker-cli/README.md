# Docker CLI

#### Most popular Docker CLI commands:
- docker ps -a (docker container ls -a)
- docker ps -aq
- docker ps -s
- docker rm -f $(docker ps -aq)
- docker image ls (docker images)
- docker container run [image] (docker run [image])
- docker run --name [image] [container-name]
- docker logs -f [container-id]
- docker inspect [image]
- docker run -it [image]
- docker inspect [container-id]
- docker run --rm [image]
- docker stats [container-id]
- docker run -p 8080:80 --name [image] [container-name]
- docker run -p 8080:80 -v [working-directory]:[in-docker-path] [image] (example in power shell: docker run -p 8080:80 -v ${pwd}:/usr/share/nginx/html nginx)
- docker run -p 8080:80 -v [working-directory]:[in-docker-path] [image] [command] (example: docker run -p 8080:80 -v ${pwd}:/app python python3 app/hello.py
- docker run --name [image] -d
#### Example:
- docker run -p 8080:80 -v ${pwd}:/usr/share/nginx/html nginx
- docker run -p 8080:80 -v ${pwd}:/app python python3 app/hello.py
- docker run --name mysql -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=my_password mysql:8
- docker logs [image] --follow (docker logs [container-id])
- docker exec -it [image] [command] (example: docker exec -it mysql mysql -p)
- docker stop [container-id]
- docker rm [container-id]
- 

Docker CLI (Command Line Interface) is a tool that allows you to interact with the Docker daemon and manage Docker containers, images, networks, and volumes using commands in a terminal or command prompt.

#### Here are some of the most common Docker CLI commands:

- **[docker run](https://github.com/shounoop/docker/tree/main/docker-cli/docker-run)** - run a container from a Docker image.
- **[docker build](https://github.com/shounoop/docker/tree/main/docker-cli/docker-build)** - build a Docker image from a Dockerfile.
- **[docker pull](https://github.com/shounoop/docker/tree/main/docker-cli/docker-pull)** - download a Docker image from a registry.
- **[docker push](https://github.com/shounoop/docker/tree/main/docker-cli/docker-push)** - upload a Docker image to a registry.
- **[docker ps](https://github.com/shounoop/docker/tree/main/docker-cli/docker-ps)** - list running Docker containers.
- **[docker stop](https://github.com/shounoop/docker/tree/main/docker-cli/docker-stop)** - stop a running Docker container.
- **[docker rm](https://github.com/shounoop/docker/tree/main/docker-cli/docker-rm)** - remove a stopped Docker container.
- **[docker rmi](https://github.com/shounoop/docker/tree/main/docker-cli/docker-rmi)** - remove a Docker image.
- **[docker exec](https://github.com/shounoop/docker/tree/main/docker-cli/docker-exec)** - execute a command inside a running Docker container.
- **[docker logs](https://github.com/shounoop/docker/tree/main/docker-cli/docker-logs)** - view the logs of a running Docker container.
- **[docker network](https://github.com/shounoop/docker/tree/main/docker-cli/docker-network)** -
- **[docker-compose](https://github.com/shounoop/docker/tree/main/docker-cli/docker-compose)** -
- **docker start** -

You can also use Docker CLI to manage networks and volumes, build images from Dockerfiles, and manage Docker swarms for container orchestration.

Overall, Docker CLI is a powerful tool for managing Docker containers and images from the command line. It is widely used by developers, DevOps engineers, and system administrators to build, deploy, and manage containerized applications.
