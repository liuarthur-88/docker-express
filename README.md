# Official express-generator
## Step-by-step:
1. Use npx to run express-generator:
```
    npx express-generator myapp
```
2. Navigate to the project:
```
    cd myapp
```
3. Install dependencies:
```
    npm install
```
4. Run the app:
```
    npm start
```
5. By default, this sets up:
```
    app.js
    bin/www (startup script)
    View engine (Pug)
    Routing structure
    Middleware and error handling
```

---

# GitHub
## Initialize Git and Set Remote
```
    git init .
    git remote add origin git@github.com:username/repo.git
```

## Commit the Code
```
    git add .
    git commit -m "initial commit"
```

## Push to GitHub
```
    git branch -M main
    git push -u origin main
```

## Tag the Commit (Optional)
```
    git tag initial-commit
    git push origin initial-commit
```

## Final Version (Best Practice)
```
    git init
    git remote add origin git@github.com:username/repo.git

    git add .
    git commit -m "initial commit"

    git branch -M main
    git push -u origin main

    git tag initial-commit
    git push origin initial-commit
```

---

# Docker

## Initialize Docker in Your Project

1. Open the Command Palette with `Ctrl+Shift+P` and run the command:  
   `Containers: Add Docker Files to Workspace...`
2. Select **Node.js** when prompted for the application platform.
3. Choose the default `package.json` file.
4. Enter `3000` when prompted for the application port.
5. Choose **Yes** or **No** when asked whether to include Docker Compose files.  
   > Docker Compose is typically used when managing multiple services or containers.

## Add an Environment Variable to the Image

1. Open the `Dockerfile`.
2. Use the `ENV` instruction to add environment variables, example:
```
    ENV NODE_ENV=production
```

3. Save the `Dockerfile`.

## Build the Service Image

1. Open the Command Palette with `Ctrl+Shift+P` and run:
   `Container Images: Build Image...`
2. Open the **Container Explorer** and verify that the newly built image appears in the **Images** view.

## Run the Service Container

1. In the **Container Explorer**, right-click the image you built and choose **Run** or **Run Interactive**.
2. The container will start, and it should appear in the **Containers** view.

## Common Docker Commands

* **List images:**

```
    docker images
```

* **Remove an image:**

```
    docker rmi your-image-name
```

* **Build and tag an image:**

```
    docker build -t username/your-image-name:v1.0.1 .
```

  After building, verify the image in the **Images** view.

* **Push an image to Docker Hub:**

```
    docker push username/your-image-name:v1.0.1
```

## Reading a Local `sys-config.json` File in a Container

To make a local `sys-config.json` file available inside a container:

```
docker run --rm -v C:\path\to\sys-config.json:/app/sys-config.json your-image-name
```

> Replace `C:\path\to\sys-config.json` with the actual path to your file.
> On macOS/Linux, use `$(pwd)/sys-config.json` instead.

---