# docker build

The docker build command is used to build a Docker image from a Dockerfile. You can specify the tag name for the image and the build context (i.e., the directory where the Dockerfile is located).

For example, to build a Docker image with the tag name myimage:latest from the current directory (.), you can use the following command:

```cmd
docker build -t myimage:latest .
```
