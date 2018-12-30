## Part 1

### 1.1

```
$ docker ps -a

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                      PORTS               NAMES
6cd47fe211af        nginx               "nginx -g 'daemon of…"   13 minutes ago      Exited (0) 12 minutes ago                       mystifying_wiles
c79191a359bb        nginx               "nginx -g 'daemon of…"   13 minutes ago      Exited (0) 13 minutes ago                       zen_stonebraker
c9fd38094ab9        nginx               "nginx -g 'daemon of…"   14 minutes ago      Up 13 minutes               80/tcp              practical_cohen
```

### 1.2

```
$ docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
````

```
$ docker images

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
```

### 1.3

Start a ubuntu image. The container will be named exercise-1-3:
```
$ docker run -d -it --name exercise-1-3 ubuntu:16.04 sh -c 'read website; sleep 3; curl http://$website;'
```
Install curl in the container:
```
$ docker exec exercise-1-3 apt-get update
...
$ docker exec exercise-1-3 apt-get install -y curl
...
```
Attach to the container:
```
$ docker attach exercise-1-3
```
Type the name of the website to ```curl```:
```
helsinki.fi
```
The response is:
```
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
```

### 1.4

The Dockerfile: [Dockerfile](/Files/Exercise-1-4/Dockerfile)

The script: [curlscript.sh](/Files/Exercise-1-4/curlscript.sh)

Build Docker image:
```
$ docker build -t curler .
```
Run Docker container:
```
$ docker run -it curler
```
Type the name of the website to ```curl```:
```
helsinki.fi
```
The response is:
```
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
```

### 1.5

The Dockerfile: [Dockerfile](/Files/Exercise-1-5/Dockerfile)

Build Docker image:
```
$ docker build -t frontend .
```
Run Docker container:
```
$ docker run -d -p 5000:5000 frontend
```
The service will be in: http://localhost:5000

### 1.6

The Dockerfile: [Dockerfile](/Files/exercise-1-6/Dockerfile)

Build Docker image:
```
$ docker build -t backend .
```
Create local log file and then run Docker container:

(*Need to have the double quotes around* ```$(pwd)``` *if you have uppercase characters (or spaces) in your path*)
```
$ touch logs.txt
$ docker run -d -v "$(pwd)"/logs.txt:/exercise/logs.txt -p 8000:8000 backend
```
The service responds in: http://localhost:8000

The log output: [logs.txt](/Files/exercise-1-6/logs.txt)

### 1.7

The backend Dockerfile: [DockerfileBackend](/Files/exercise-1-7/DockerfileBackend)

The frontend Dockerfile: [DockerfileFrontend](/Files/exercise-1-7/DockerfileFrontend)

Build Docker images:
```
$ docker build -t backend -f DockerfileBackend .
$ docker build -t frontend -f DockerfileFrontend .
```
Create local log file and then run Docker containers:
```
$ touch logs.txt
$ docker run -d -v "$(pwd)"/logs.txt:/exercise/logs.txt -p 8000:8000 backend
$ docker run -d -p 5000:5000 frontend
```
The frontend service responds in http://localhost:5000

The backend service responds in http://localhost:8000

The log output: [logs.txt](/Files/exercise-1-7/logs.txt)




