<h1 align="center"> DevSecOps-Workflow-With-Mern-Stack-Application ♾️🛡️ </h1>

<br>

## Pre-Requisite : ##

<b> • VS Code (Your intuitive code editor) </b> <br>
<b> • Git (Reliable version control for your code) </b> <br>
<b> • GitHub (Collaborative code repository) </b> <br>
<b> • Docker (Containerization made simple) </b> <br>
<b> • Helm (Orchestrate Kubernetes with ease) </b> <br>
<b> • Trivy (Quick vulnerability scanning) </b> <br>
<b> • Kubelinter (Linting for Kubernetes best practices) </b> <br>
<b> • Kyverno (Policy management for Kubernetes) </b> <br>
<b> • Flux CD (Automated GitOps deployment) </b> <br>
<b> • AKS (Managed Kubernetes on Azure) </b> <br>
<b> • Falco (Real-time cloud security monitoring) </b> <br>

<br>

<h3 align="center"> Let's Begin ✌🏻 </h3>

<br>

<h3 align="center"> 1) Build & Compose Mern Application With Docker : </h3>

<br>

### Check Out Following Docker Images :-

<a href="mern/frontend/Dockerfile">frontend</a>
<a href="mern/backend/Dockerfile">backend</a>

### Create a network for the docker containers

`docker network create demo`

### Build the client 

```sh
cd mern/frontend
docker build -t mern-frontend .
```

### Run the client

`docker run --name=frontend --network=demo -d -p 5173:5173 mern-frontend`

### Verify the client is running

Open your browser and type `http://localhost:5173`

### Run the mongodb container

`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongo:latest`

### Build the server

```sh
cd mern/backend
docker build -t mern-backend .
```

### Run the server

`docker run --name=backend --network=demo -d -p 5050:5050 mern-backend`

## Using Docker Compose

`docker compose up -d`

<br>
