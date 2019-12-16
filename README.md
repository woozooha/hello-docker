# Docker sample

## docker build
```
$ docker build -t hello-docker .
```
```
Sending build context to Docker daemon  58.88kB
Step 1/3 : FROM alpine
 ---> 965ea09ff2eb
Step 2/3 : COPY script.sh /script.sh
 ---> 1f0199abc27e
Step 3/3 : CMD ["/script.sh"]
 ---> Running in 7cf3034b9fdd
Removing intermediate container 7cf3034b9fdd
 ---> 5b5a01308ddb
Successfully built 5b5a01308ddb
Successfully tagged hello-docker:latest
```

## docker run

```
$ docker run --rm --name test hello-docker
```
```
Hello World! from the script file!
```

## docker exec

```
$ docker exec -it test bin/sh
```
```
/ # ls
bin        etc        lib        mnt        proc       run        script.sh  sys        usr
dev        home       media      opt        root       sbin       srv        tmp        var
/ # exit
```

## docker ps
```
$ docker ps
```
```
CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS              PORTS               NAMES
0fc9c1389f41        hello-docker        "/script.sh"        About a minute ago   Up About a minute  
```

## docker stop
```
$ docker stop test
```
```
test
```
