# Docker
## Init Docker
1. Open the Command Palette `Ctrl+Shift+P` and use `Containers: Add Docker Files to Workspace...` command
2. Select `Node.js` when prompted for the application platform.
3. Choose the default `package.json` file.
4. Enter `3000` when prompted for the application port.
5. Select either `Yes` or `No` when prompted to include Docker Compose files. Compose is typically used when running multiple containers at once.

## Add an environment variable to the image
1. Open the `Dockerfile` file.
2. Use ENV instruction to add an environment variable to the service container image.
3. Save the `Dockerfile` file.

## Build the service image
1. Open the Command Palette `Ctrl+Shift+P` and select the `Container Images: Build Image...` command.
2. Open the `Container Explorer` and verify that the new image is visible in the `Images` view

## Run the service container
1. Right-click on the image built in the previous section and select `Run` or `Run Interactive`. The container should start and you should be able to see it in the `Containers` view

## Docker command
1. List images: `docker images`
2. Remove image: `docker rmi your-image-name`
3. Build and Tag: `docker build -t username/your-image-name:v1.0.1 .`, open the `Container` explorer and verify that the new image is visible in the `Images` view
4. Push image to Docker Hub: `docker push username/your-image-name:v1.0.1`