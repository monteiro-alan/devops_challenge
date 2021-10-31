# Done by Álan Monteiro 
- Created ./resources folder
- Created Dockerfiles from services
- Created Docker-compose files
- Changed DB connection and query in ./api/app.js
- Created .dockerignore files
- Added nodemon in package.json files for debug

# Running
- Clone the project:
````shell
git clone https://github.com/monteiro-alan/devops_challenge.git
````

- Change to dir "resources": 
````shell
cd devops_challenge/resources
````

- Create a ".env" file with environment variables. You can use ".env.example" as an example: 
````shell
cp .env.example .env
````

- Start the apps: 
````shell
docker-compose up -d
````

- Open a web browser and type "http://localhost:8080/" to test the app


# About DevOps Challenge

- This repo contains code for a multilayer application.

- The application overview is as follows: web <=> api <=> db

- There is an api directory and another web, you should dock the application in the best possible way.

- Write a recipe with the tool of your choice (ansible or terraform) to build the environment and run the application in an automated way.

# Running

- The idea to test locally is to just run 'docker-compose up'
- Access url localhost: 8080


# Evaluation

- It will count the quality of 'Dockerfile', 'docker-compose.yml'
- Extra points if you use terraform and are in good practice
- Extra points if you use ansible and are well structured