# Docker - Build once, run anywhere

#### I. Overview

- Docker is a tool that helps package and deploy applications in an easy, reliable and portable way. It enables developers and system administrators to create containers that hold applications and their dependencies, which can run on any environment supported by Docker.
- A Docker container is an isolated environment that contains all the libraries and tools necessary to run you application. By using Docker, you can package your application and its dependencies into a container, then deploy that container on any server supported by Docker, helping to minimize the differences between different deployment environments.
- Dock also provides users with a library of pre-build images. allowing you to start containers from these images instead of building them from scratch. This saves time and effort in the deployment process.

> In summary, Docker is a powerful tool that simplifies the process of packing and deploying your application across different evironments, as well as increasing the mobility and reliablity of your application.

#### II. Table of content about Dockerfile

| Topic               | Description                                                                                                                                                                                                                                                                         |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Containerization    | Containerization is the process of packaging an application and its dependencies into a container that can run consistently across different computing environments.                                                                                                                |
| Docker Architecture | Docker architecture consists of the Docker daemon, Docker client, Docker registry, and Docker containers.                                                                                                                                                                           |
| Docker CLI          | Docker CLI is the command-line tool used to interact with Docker (various Docker CLI commands, such as building images, starting and stopping containers, and managing Docker networks)                                                                                             |
| Docker Images       | A Docker image is a pre-built package that contains all the necessary files and dependencies to run a container (how to build, pull, and push Docker images)                                                                                                                        |
| Docker Containers   | A Docker container is a running instance of a Docker image (how to create, start, stop, and manage Docker containers)                                                                                                                                                               |
| Docker Volumes      | Docker volumes are used to store data outside of a container, making it persistent even after the container is deleted (how to create and manage Docker volumes)                                                                                                                    |
| Docker Networking   | Docker networking allows containers to communicate with each other and the outside world (how to create and manage Docker networks)                                                                                                                                                 |
| Docker Compose      | Docker Compose is a tool that allows you to define and run multi-container Docker applications (how to use Docker Compose to define and run applications)                                                                                                                           |
| Dockerfile          | - A Dockerfile is a script that contains instructions for building a Docker image.                                                                                                                                                                                                  |
|                     | - Dockerfile is a simple text file that contains instructions to build a Docker image. It provides a way to create custom Docker images to run your applications in independent containers.                                                                                         |
|                     | - A Dockerfile can be divided into several parts, each part performing a specific task during the build process of the Docker image. The instructions in the Dockerfile specify the base image, dependencies, configurations, and commands to run when the container is started.    |
|                     | - Dockerfile simplifies the process of building and deploying applications in Docker containers. By creating a Dockerfile, you can automate the process of building and deploying your application, which saves time and eliminates errors that may occur during manual deployment. |
|                     | - Overall, Dockerfile is an essential tool for creating and managing Docker containers, and it's essential to learn how to use it effectively when working with Docker.                                                                                                             |
| Docker Swarm        | Docker Swarm is a tool used to orchestrate and manage a cluster of Docker nodes (how to use Docker Swarm to manage a cluster of Docker nodes)                                                                                                                                       |
| Docker Registry     | Docker Registry is a storage and distribution system for Docker images (how to use Docker Registry to store and distribute Docker images)                                                                                                                                           |

#### III. Some of the most popular Docker commands:

- **[docker run](https://github.com/shounoop/docker/tree/main/commands/docker-run)** - run a container from a Docker image.\
- **[docker build](https://github.com/shounoop/docker/tree/main/commands/docker-build)** - build a Docker image from a Dockerfile.\
- **[docker pull](https://github.com/shounoop/docker/tree/main/commands/docker-pull)** - download a Docker image from a registry.\
- **[docker push](https://github.com/shounoop/docker/tree/main/commands/docker-push)** - upload a Docker image to a registry.\
- **[docker ps](https://github.com/shounoop/docker/tree/main/commands/docker-ps)** - list running Docker containers.\
- **[docker stop](https://github.com/shounoop/docker/tree/main/commands/docker-stop)** - stop a running Docker container.\
- **[docker rm](https://github.com/shounoop/docker/tree/main/commands/docker-rm)** - remove a stopped Docker container.\
- **[docker rmi](https://github.com/shounoop/docker/tree/main/commands/docker-rmi)** - remove a Docker image.\
- **[docker exec](https://github.com/shounoop/docker/tree/main/commands/docker-exec)** - execute a command inside a running Docker container.\
- **[docker logs](https://github.com/shounoop/docker/tree/main/commands/docker-logs)** - view the logs of a running Docker container.\
- **[docker network](https://github.com/shounoop/docker/tree/main/commands/docker-network)** - \
- **[docker-compose](https://github.com/shounoop/docker/tree/main/commands/docker-compose)** - \
- **docker start** -

## IV. [Dockerfile](https://github.com/shounoop/docker/tree/main/dockerfile)

- Dockerfile is a simple text file that contains instructions to build a Docker image. It provides a way to create custom Docker images to run your applications in independent containers.

- A Dockerfile can be divided into several parts, each part performing a specific task during the build process of the Docker image. The instructions in the Dockerfile specify the base image, dependencies, configurations, and commands to run when the container is started.

- Dockerfile simplifies the process of building and deploying applications in Docker containers. By creating a Dockerfile, you can automate the process of building and deploying your application, which saves time and eliminates errors that may occur during manual deployment.

- Overall, Dockerfile is an essential tool for creating and managing Docker containers, and it's essential to learn how to use it effectively when working with Docker.
