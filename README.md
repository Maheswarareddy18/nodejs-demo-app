# nodejs-demo-app 
The objective of this task is to automate the deployment process for a sample application using a CI/CD pipeline configured with GitHub Actions. This ensures that whenever code is pushed or updated in the GitHub repository, the entire deployment cycle—testing, building, and containerizing the application—is executed automatically and reliably.
GitHub Actions – For Continuous Integration / Continuous Deployment (CI/CD)

Node.js – Sample application used for this task

Docker – To build and run the application in isolated containers

DockerHub – To store and distribute built Docker images
 Code Push Triggers the Pipeline
The pipeline starts automatically whenever a developer pushes changes to the main branch of the GitHub repository.

 Checkout Source Code
GitHub Actions checks out the latest version of the code from the repository to run the workflow steps.

 Install Dependencies
Node.js dependencies are installed to ensure the application has all the packages required to run.

 Run Tests
The pipeline executes any unit or functional tests to ensure code quality and correctness. If tests fail, the pipeline stops here.

 Docker Image Build
A Docker image of the application is built using a Dockerfile defined in the project.

This image contains the complete application and all of its dependencies.

 DockerHub Authentication
 The workflow uses encrypted GitHub Secrets to securely log in to DockerHub.

 Push Docker Image to DockerHub
Once the image is built, it is pushed to DockerHub under the developer’s repository.

This allows the image to be deployed to any containerized platform later.


