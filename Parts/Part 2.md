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

The log output: [logs.txt](/Files/Exercise-2-1/logs.txt)


