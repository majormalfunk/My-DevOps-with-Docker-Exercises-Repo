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
$ docker run -d -it --name exercise-1-3 ubuntu:16.04
```
Enter the container and install curl:
```
$ docker exec -it exercise-1-3 bash
root@a3c669923f9a:/# apt-get update
...
root@a3c669923f9a:/# apt-get install curl
...
```
Exit the container:
```
root@a3c669923f9a:/# exit
```
Start the process in the container:
```
$ docker exec -it exercise-1-3 sh -c 'read website; curl http://$website;'
```








