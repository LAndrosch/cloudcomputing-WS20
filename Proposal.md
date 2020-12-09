# Project in Cloud Computing

## Current state
There is an existing Application, which consists out of three parts 

- Client
	
- Server

- Database

The original intention was a progressive web application that has the a simple archtiecture and is implemented in Angular.

	The server and the database represent the backend, where the server retrieves and stores information on the database. 

	The client does only interact with the server and is used as UI.

## Goal of the Project

- Create Docker files for every part of the application
	
	- Create a docker image for both, client and server
	- For the database a docker mongoDB image is used 
	- Run the whole application using Docker

- Implement a Continues Integration using GitHub Actions

	- Use CI to create new versions of client and server
