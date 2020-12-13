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

	- On a new release GitHub Actions should take care of pushing the new docker images to DockerHub
	- Additionally an existing shared codebase between server and client should be automatically published on NPM
