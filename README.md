# Simple Node.js App

Welcome to Simple Node.js App, a lightweight and straightforward Node.js application!

## Overview

Simple Node.js App is designed to provide a minimalistic yet functional starting point for Node.js development. It includes essential files and configurations to help you quickly set up and run a basic Node.js application.

## Features

- Minimalistic Node.js application setup.
- Docker configuration for containerization.
- Basic file structure including index.js, package.json, Dockerfile, and README.md.
- Easy to customize and extend for your specific needs.

## Installation

To get started with Simple Node.js App, follow these steps:

1. Clone this repository to your local machine:

   git clone https://github.com/kamranali111/simple-nodejs-app.git

Navigate into the project directory:
b

cd simple-nodejs-app

2. Dockerfile:

======================================================

FROM node

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]

======================================================

3. Build the Docker image:

docker build -t my-node-app .
To check created Docker images, run the command docker images.

4. Run the Docker container:

docker run -d -p 8080:3000 my-node-app

The application will be accessible at http://localhost:8080 in your web browser.

To check your source code in the container, run:


5. docker run -it my-node-app /bin/bash

6. ls