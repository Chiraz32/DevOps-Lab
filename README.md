## Jenkins Pipeline Demo Repository

This repository showcases an implementation of a Jenkins pipeline designed to automate the build, push, and deployment processes for a Node.js application. 
The pipeline is configured to utilize Docker for containerization and ensures a seamless CI/CD workflow.

### Pipeline Stages

1. **Build**: This stage builds the Docker image using the specified Dockerfile located at `nodejs-app/Dockerfile`.
2. **Push**: Once the image is built, it is pushed to the Docker registry using the provided credentials.
3. **Run**: Finally, the Docker image is run, exposing it on port 80 and naming the container `learning-app-jenkins`.

### Environment Variables

- `registry`: Specifies the Docker registry to which the image will be pushed.
- `registryCredential`: The Jenkins credential ID for authenticating with the Docker registry.
- `dockerImage`: A variable to hold the Docker image object.
- `dockerfilePath`: Path to the Dockerfile used for building the image.

