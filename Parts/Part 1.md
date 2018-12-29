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

[Dockerfile](My-DevOps-with-Docker-Exercises-Repo/Files/Exercise-1-4/Dockerfile)
[curlscript.sh](My-DevOps-with-Docker-Exercises-Repo/Files/Exercise-1-4/curlscript.sh)

Build Docker image:
```
$ docker build -t curler .
```
Run Docker image:
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


