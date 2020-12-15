# Project in Cloud Computing

## Current state
There is an existing Application, which consists out of three parts 

- Client (Angular Frontend)
	
- Server (NodeJS Backend)

- Database (MongoDB)

The original intention was a progressive web application that has a simple architecture and is implemented in NodeJS and Angular (original project by Setre14 and thedarthmader).

	The server and the database represent the backend, where the server retrieves and stores information on the database. 

	The client does only interact with the server and is used as UI.

## Goal of the Project

The goal of the project is to implement a Continous Integration which builds docker images on every new release for all the components. 

The steps that should be taken are therefore:

- Create and use Docker
	
	- Create docker images for the client and the server
	- For the database an existing MongoDB image will be used
	- Run the whole application using Docker

- Implement a Continues Integration using GitHub Actions

	- ~~On a new release GitHub Actions should take care of pushing the new docker images to DockerHub~~
	- ~~Additionally an existing shared codebase between server and client should be automatically published on NPM~~
		
	- In a **GitFlow approach** on every new release, the CI should automatically push the newly built docker images to DockerHub
	- The shared codebase between server and client should be **automatically published to NPM** 
	- To verify the quality of the codebase, some steps should be taken on every push/merge to master <br>
	**Snyk** should be used to automatically check the npm module against security flaws on every push/merge to the master
	
- Providing a theoretical POC for publishing the newly created docker images on a kubernetes cluster

	We are not yet sure, if we really want to run the application in the cloud, however we want to provide the necessary infrastructure/workflows
