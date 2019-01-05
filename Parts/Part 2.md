## Part 2

### 2.1

The backend Dockerfile: [DockerfileBackend](/Files/Exercise-2-1/DockerfileBackend) \
The frontend Dockerfile: [DockerfileFrontend](/Files/Exercise-2-1/DockerfileFrontend) \
The docker-compose file: [docker-compose.yml](/Files/Exercise-2-1/docker-compose.yml)

Build Docker images:
```
$ docker-compose build
```
Create local log file and then run Docker containers:
```
$ touch logs.txt
$ docker-compose up -d
```
The frontend service responds in http://localhost:5000 \
The backend service responds in http://localhost:8000

### 2.2

The backend Dockerfile: [DockerfileBackend](/Files/Exercise-2-2/DockerfileBackend) \
The frontend Dockerfile: [DockerfileFrontend](/Files/Exercise-2-2/DockerfileFrontend) \
The docker-compose file: [docker-compose.yml](/Files/Exercise-2-2/docker-compose.yml)

Build Docker images:
```
$ docker-compose build
```
Create local log file and then run Docker containers:
```
$ touch logs.txt
$ docker-compose up -d
```
The frontend service responds in http://localhost:5000 \
The backend service responds in http://localhost:8000

### 2.3

The backend Dockerfile: [DockerfileBackend](/Files/Exercise-2-3/DockerfileBackend) \
The frontend Dockerfile: [DockerfileFrontend](/Files/Exercise-2-3/DockerfileFrontend) \
The docker-compose file: [docker-compose.yml](/Files/Exercise-2-3/docker-compose.yml)

Build Docker images:
```
$ docker-compose build
```
Create local log file and then run Docker containers:
```
$ touch logs.txt
$ docker-compose up -d
```
The frontend service responds in http://localhost:5000 \
The backend service responds in http://localhost:8000

### 2.4
The docker-compose file: [docker-compose.yml](/Files/Exercise-2-4/docker-compose.yml)

Clone the repositories (*Couldn't make this work in docker-compose*):
```
git clone git@github.com:docker-hy/ml-kurkkumopo-training.git
git clone git@github.com:docker-hy/ml-kurkkumopo-backend.git
git clone git@github.com:docker-hy/ml-kurkkumopo-frontend.git
```
Build Docker images:
```
$ docker-compose build
```
Run Docker containers:
```
$ docker-compose up -d
```

### 2.5

The backend Dockerfile: [DockerfileBackend](/Files/Exercise-2-5/DockerfileBackend) \
The frontend Dockerfile: [DockerfileFrontend](/Files/Exercise-2-5/DockerfileFrontend) \
The docker-compose file: [docker-compose.yml](/Files/Exercise-2-5/docker-compose.yml) \
The nginx configuration file: [nginx.conf](/Files/Exercise-2-5/nginx.conf)

Build Docker images:
```
$ docker-compose build
```
Create local log file and then run Docker containers:
```
$ touch logs.txt
$ docker-compose up -d
```
The frontend service responds in http://localhost:5000 \
The backend service responds in http://localhost:8000
