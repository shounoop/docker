# docker run

The docker run command is used to create and start a new container from a specified Docker image. Here's a basic syntax for the docker run command:

```cmd
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```

Let's break down each part of this command:

- docker run: This is the command to create and start a new container.
- [OPTIONS]: This is where you can specify various options for the docker run command. Some commonly used options include:
  - -d: This option runs the container in the background (detached mode).
  - -it: Allows you to run an interactive terminal session inside a container.
  - -p: This option maps a container port to a host port.
  - -v: This option mounts a host directory or file as a volume in the container.
  - --name: This option gives a name to the container.
  - --rm: This option removes the container when it is stopped.
  - IMAGE: This is the name of the Docker image that you want to use to create the container.
- [COMMAND] [ARG...]: This is an optional command that you can use to specify a command to run inside the container. If you don't specify a command, Docker will use the default command specified in the Dockerfile for the image.

#### Examples:

Here's an example of how to use the docker run command:

```cmd
docker run -d -p 8080:80 --name myapp nginx
```

In this example, we're using the nginx image to create a new container named myapp. We're also using the -d option to run the container in detached mode and the -p option to map port 8080 on the host to port 80 inside the container.

Once you run the docker run command, Docker will pull the specified image from a registry (such as Docker Hub), create a new container from that image, and start the container. You can then use other Docker CLI commands (such as docker ps, docker stop, and docker rm) to manage the container.

**Naming container**:

```cmd
docker run -d -p 8080:80 --name mynginx nginx
```

- This command will start a Docker container named "mynginx" that runs the official Nginx web server image.\
- The --name option sets the name of the container to "mynginx".

**Start a Docker contain** + **naming container** + **Mounting a directory** from the host machine to a directory in the container

```cmd
docker run -d -p 8080:80 --name mynginx -v "D:\docker\commands\docker-run\html":/usr/share/nginx/html nginx
```

- The -v option mounts a directory from the host machine to a directory in the container. In this case, it mounts the directory D:\docker\commands\docker-run\html on the host to the directory /usr/share/nginx/html in the container. This means that any files placed in the html directory on the host will be served by the Nginx server running in the container.
- Finally, the command specifies the name of the Docker image to run, which is "nginx".

**Using -it option**:
When you run a container with the -it option, you'll be dropped into a shell prompt inside the container, and you can execute commands just as you would in a regular terminal.
Here's an example of how to use the -it option with the docker run command:

```cmd
docker run -it ubuntu bash
```

In this example, we're using the ubuntu image to create a new container, and we're specifying the bash command as the command to run inside the container. The -it option tells Docker to start an interactive terminal session inside the container.

When you run this command, you'll be dropped into a shell prompt inside the container, and you can execute commands just as you would in a regular terminal. For example, you can run the ls command to list the contents of the current directory inside the container:

```cmd
root@7c77dd6a8f7e:/# ls
bin  boot  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
```

Once you're done with the interactive terminal session, you can exit the container by typing exit at the shell prompt.

The -it option is useful for debugging and troubleshooting containerized applications, as it allows you to run commands inside the container and inspect its state.
