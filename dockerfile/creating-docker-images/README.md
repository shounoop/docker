# Creating Docker Images

### Dockerfile Instructions

As mentioned earlier, a Dockerfile contains a set of instructions that are executed in order to create a Docker image. These instructions can be used to add files, run commands, and install dependencies. Let's go through some commonly used instructions in a Dockerfile.

- _FROM_

  The FROM instruction specifies the base image that will be used for the new image. This is usually an operating system with some pre-installed software. For example, to use the official Node.js image, you can add the following line to your Dockerfile:

  ```Dockerfile
  FROM node:14-alpine
  ```

  This will use the Node.js 14 Alpine image as the base image for your new image.

- _WORKDIR_
  The WORKDIR instruction sets the working directory for subsequent instructions. For example, to set the working directory to /app, you can add the following line to your Dockerfile:

  ```Dockerfile
  WORKDIR /app
  ```

- _COPY_
  The COPY instruction copies files from the host machine to the Docker image. For example, to copy package.json and package-lock.json from the current directory to the /app directory in the Docker image, you can add the following line to your Dockerfile:

  ```Dockerfile
  COPY package*.json ./
  ```

- _RUN_
  The RUN instruction runs a command in the Docker image. For example, to install dependencies using npm, you can add the following line to your Dockerfile:

  ```Dockerfile
  RUN npm install
  ```

- _EXPOSE_
  The EXPOSE instruction exposes a port for the Docker container. For example, to expose port 3000, you can add the following line to your Dockerfile:

  ```Dockerfile
  EXPOSE 3000
  ```

- CMD
  The CMD instruction specifies the command to run when the Docker container starts. For example, to start a Node.js application, you can add the following line to your Dockerfile:

  ```Dockerfile
  CMD ["npm", "start"]
  ```

### Creating a Docker Image using a Dockerfile

To create a Docker image using a Dockerfile, you can use the docker build command. This command reads the Dockerfile from the current directory and builds a Docker image based on the instructions in the Dockerfile.

Here's an example of how to create a Docker image for a Node.js application using the Dockerfile we created earlier:

1. Create a directory for your Node.js application and navigate to that directory in the terminal.

2. Create a Dockerfile in the directory and add the instructions for your Docker image.

3. Run the following command in the terminal to build the Docker image:

   ```cmd
   docker build -t my-node-app .
   ```

   The -t flag specifies the name and tag of the Docker image (my-node-app in this example), and the . specifies the current directory as the build context.

4. Once the build is complete, you can run the Docker container using the following command:

   ```cmd
   docker run -p 3000:3000 my-node-app
   ```

   This command runs the Docker container and maps port 3000 in the Docker container to port 3000 on the host machine. The container will start running the command specified in the CMD instruction in the Dockerfile (in this case, npm start).

--> **Congratulations! You have now created a Docker image for your Node.js application and run it in a Docker container.**
