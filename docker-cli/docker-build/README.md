# docker build

The _docker build_ command is used to build a Docker image from a Dockerfile. You can specify the tag name for the image and the build context (i.e., the directory where the Dockerfile is located).

#### The basic syntax of the _docker build_ command is:

```cmd
docker build [OPTIONS] PATH
```

Here's a breakdown of the different components of this command:

- OPTIONS: These are additional options that can be passed to the _docker build_ command. Some commonly used options include:
  - -t IMAGE_NAME:TAG: This specifies the name and tag for the Docker image being built.
  - -f DOCKERFILE_PATH: This specifies the path to the Dockerfile to use for building the image.
  - --no-cache: This tells Docker to not use the cache when building the image, which can be useful for ensuring that all dependencies are up-to-date.
- PATH: This is the path to the build context, which is the directory that contains the Dockerfile and any other files needed for building the image.

When you run the _docker build_ command, Docker will read the Dockerfile in the build context and execute the instructions in the order they are listed in the Dockerfile. Each instruction creates a new layer in the Docker image.

Here's an example of how to build a Docker image using the _docker build_ command:

```cmd
docker build -t my-image:latest .
```

This command builds a Docker image with the tag my-image:latest using the Dockerfile in the current directory (.). Once the build is complete, you can run a container from the image using the docker run command:

```cmd
docker run my-image:latest
```

This will start a new container from the my-image:latest image.
