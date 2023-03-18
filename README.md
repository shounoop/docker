# Docker - Build once, run anywhere

## Overview

- Docker is a tool that helps package and deploy applications in an easy, reliable and portable way. It enables developers and system administrators to create containers that hold applications and their dependencies, which can run on any environment supported by Docker.
- A Docker container is an isolated environment that contains all the libraries and tools necessary to run you application. By using Docker, you can package your application and its dependencies into a container, then deploy that container on any server supported by Docker, helping to minimize the differences between different deployment environments.
- Dock also provides users with a library of pre-build images. allowing you to start containers from these images instead of building them from scratch. This saves time and effort in the deployment process.

> In summary, Docker is a powerful tool that simplifies the process of packing and deploying your application across different evironments, as well as increasing the mobility and reliablity of your application.

## Some of the most popular Docker commands:

docker run - run a container from a Docker image.\
docker build - build a Docker image from a Dockerfile.\
docker pull - download a Docker image from a registry.\
docker push - upload a Docker image to a registry.\
docker ps - list running Docker containers.\
docker stop - stop a running Docker container.\
docker rm - remove a stopped Docker container.\
docker rmi - remove a Docker image.\
docker exec - execute a command inside a running Docker container.\
docker logs - view the logs of a running Docker container.\

##

- **docker run**:
  The docker run command is used to run a Docker container from a Docker image. You can specify the image name and any additional options you want to use with the container. For example, to run a container from the official Nginx image in detached mode (-d) and map the container port 80 to the host port 80 (-p 80:80), you can use the following command:

  ```cmd
  docker run -d -p 80:80 nginx
  ```

- **docker build**:
  The docker build command is used to build a Docker image from a Dockerfile. You can specify the tag name for the image and the build context (i.e., the directory where the Dockerfile is located). For example, to build a Docker image with the tag name myimage:latest from the current directory (.), you can use the following command:

  ```cmd
  docker build -t myimage:latest .
  ```

- **docker pull**:
  The docker pull command is used to download a Docker image from a registry. You can specify the image name and tag name for the image you want to download. For example, to download the latest version of the Ubuntu image from the Docker Hub registry, you can use the following command:

  ```cmd
  docker pull ubuntu
  ```

- **docker push**:
  The docker push command is used to upload a Docker image to a registry. You need to first tag the image with the name of the registry before you can push it. For example, to tag an image with the name myregistry/myimage:latest, you can use the following command:

  ```cmd
  docker tag myimage:latest myregistry/myimage:latest
  ```

  Then, you can push the image to the registry using the following command:

  ```cmd
  docker push myregistry/myimage:latest
  ```

- **docker ps**:
  The docker ps command is used to list running Docker containers. You can specify any additional options you want to use with the command. For example, to list all running containers along with their port mappings and container IDs, you can use the following command:

  ```cmd
  docker ps -a --format "table {{.ID}}\t{{.Names}}\t{{.Ports}}"
  ```

- **docker stop**:

  The docker stop command is used to stop a running Docker container. You need to specify the container ID or name of the container you want to stop. For example, to stop a container with ID CONTAINER_ID, you can use the following command:

  ```cmd
  docker stop CONTAINER_ID
  ```

- **docker rm**:

  The docker rm command is used to remove a stopped Docker container. You need to specify the container ID or name of the container you want to remove. For example, to remove a container with ID CONTAINER_ID, you can use the following command:

  ```cmd
  docker rm CONTAINER_ID
  ```

- **docker rmi**:

  The docker rmi command is used to remove a Docker image. You need to specify the tag name for the image you want to remove. For example, to remove an image with the tag name myimage:latest, you can use the following command:

  ```cmd
  docker rmi myimage:latest
  ```

- **docker exec**:

  The docker exec command is used to execute a command inside a running Docker container. You need to specify the container ID or name of the container you want to execute the command in, as well as the command you want to execute. For example, to execute the ls command inside a container with ID CONTAINER_ID, you can use the following command:

  ```cmd
  docker exec CONTAINER_ID ls
  ```

- **docker logs**:

  The docker logs command is used to view the logs of a Docker container. You need to specify the container ID or name of the container you want to view the logs for. For example, to view the logs of a container with ID CONTAINER_ID, you can use the following command:

  ```cmd
  docker logs CONTAINER_ID
  ```

- **docker network**:
  The docker network command is used to manage Docker networks. You can use it to create, list, inspect, connect, and disconnect Docker networks. For example, to create a new bridge network with the name mynetwork, you can use the following command:

  ```cmd
  docker network create mynetwork
  ```

- **docker-compose**:
  The docker-compose command is used to manage multi-container Docker applications. You can use it to define and run multi-container Docker applications using a YAML file. For example, to start a multi-container application defined in a docker-compose.yml file, you can use the following command:

  ```cmd
  docker-compose up
  ```

  This command will start all the containers defined in the docker-compose.yml file and attach them to a network named after the project directory. You can also use the docker-compose command to stop and remove the containers using the following command:

  ```cmd
  docker-compose down
  ```
