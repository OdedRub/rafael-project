Introduction

This workflow is used to automate the process of building and deploying a Java application using Maven and Docker. The workflow is triggered by a push event to the master branch or by a pull request to the master branch.


Environment

The workflow runs on ubuntu-latest and requires the following permissions: contents with write access and packages with write access.


Stages
	
The workflow consists of two stages: `build` and `run`.


Build

The `build` stage performs the following tasks:

		1. Checkout the code from the master branch of the GitHub repository.
		2. Set up JDK 8 and cache Maven dependencies.
		3. Bump the version of the jar file inside the POM file.
		4. Build a Docker image using the updated jar version as a build argument inside a multistaged-Dockerfile.
		5. Login to DockerHub with saved secrets.
		6. Push the Docker image to a given respository inDockerHub.
		7. Update the POM file with the updated jar version.



Run

The `run` stage performs the following tasks:

		1. Login to DockerHub.
		2. Run the Docker container with the image built in the `build` stage.

