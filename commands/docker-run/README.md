# docker run

The docker run command is used to run a Docker container from a Docker image. You can specify the image name and any additional options you want to use with the container.

For example:

- To **run a container** from the official Nginx image in detached mode (-d) and map the container port 80 to the host port 80 (-p 80:80), you can use the following command:

  ```cmd
  docker run -d -p 80:80 nginx
  ```

  - The -d option runs the container in detached mode, which means it will run in the background and won't output any logs or messages to the console.\
  - The -p option maps port 8080 on the host machine to port 80 in the container. This means that when you visit http://localhost:8080 in a web browser, the request will be forwarded to the Nginx server running in the container.
    <br>

- Another example using with -it option:

  ```cmd
  docker run -it -p 8080:80 nginx
  ```

  - The -it option instructs Docker to allocate a pseudo-TTY and keep STDIN open even if not attached, which means you can interact with the container's shell after it starts running.
    <br>

- **Naming container**:

  ```cmd
  docker run -d -p 8080:80 --name mynginx nginx
  ```

  - This command will start a Docker container named "mynginx" that runs the official Nginx web server image.\
  - The --name option sets the name of the container to "mynginx".
    <br>

- **Start a Docker contain** + **naming container** + **Mounting a directory** from the host machine to a directory in the container

  ```cmd
  docker run -d -p 8080:80 --name mynginx -v "D:\docker\commands\docker-run\html":/usr/share/nginx/html nginx
  ```

  - The -v option mounts a directory from the host machine to a directory in the container. In this case, it mounts the directory D:\docker\commands\docker-run\html on the host to the directory /usr/share/nginx/html in the container. This means that any files placed in the html directory on the host will be served by the Nginx server running in the container.
  - Finally, the command specifies the name of the Docker image to run, which is "nginx".
    <br>
