# Docker

### Docker Installation in Ubuntu 20.04

download latest updated package information


```shell
$ sudo apt-get update
```

```shell
$ sudo apt-get install \
               apt-transport-https \
               ca-certificates \
               curl \
               gnupg-agent \
               software-properties-common
```

```shell
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

```shell
$ sudo apt-key fingerprint 0EBFCD88
```

```shell
$ sudo add-apt-repository \
       "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
       $(lsb_release -cs) \
       stable"
```

```shell
$ sudo apt-get update
````

```shell
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```

```shell
$ sudo docker run hello-world
```

### Docker Post Installation

configure docker to start on boot
```shell
$ sudo systemctl enable docker
```

### Container Registry

Registry is a place or application that hosted docker images in the internet or cloud. Docker Hub is one example of container registry.

- Docker Docs : <https://docs.docker.com>
- Docker Hub  : <https://hub.docker.com>
- Google Container Registry       : <https://cloud.google.com/container-registry>
- AWS Elastic Container Registry  : <https://aws.amazon.com/id/ecr>

### Docker System Information
```shell
$ sudo docker info
$ sudo docker --version
$ sudo docker version
$ docker version
$ docker --version
```

### Docker Images

get list of docker images
```shell
$ sudo docker images
$ docker images
```

pull image from registry or download image from registry to local machine
```shell
$ docker pull nginx
$ sudo docker pull mongo:4.1
$ sudo docker pull mongo:4.2
```

delete docker images by ID
```shell
$ docker rmi cb81b8241902
```
delete docker images by name
```shell
$ docker rmi ubuntu
$ docker rmi nginx:alpine
```

### Docker Container

Check All container
```shell
$ docker ps -a
$ docker ps --all

$ docker container ls -all
$ docker container ls --all
$ docker container ls -a
```

Check running container
```shell
$ docker ps

$ docker container ls
```

create container from image
```shell
$ sudo docker container create --name mongoserver1 mongo:4.1
$ sudo docker container create --name mongoserver2 mongo:4.1

$ docker container create --name nginx-server nginx:latest
$ docker container create --name nginx-server -p 8080:80 nginx:latest
```

start or run docker container
```shell
$ sudo docker container start mongoserver1
$ sudo docker container start mongoserver2

$ docker container start nginx-server
```

stop docker container
```shell
$ sudo docker container stop mongoserver1
$ sudo docker container stop mongoserver1
$ docker container stop nginx-server

# stop all containers
$ sudo docker container stop mongoserver1 mongoserver2
```
stop docker container by ID
```shell
$ sudo docker container stop 69c996783ad4
```

delete docker container
```shell
$ docker container rm nginx-server

# delete container by ID
$ docker container rm e080880236a2
$ sudo docker container rm 69c996783ad4

# delete more than one container
$ sudo docker container rm mongoserver1 mongoserver2
```

Docker Help Command
```shell
$ docker container --help
$ docker images --help
$ docker --help
$ docker container ls --help
$ docker ps --help
$ docker container
```

Docker References
<https://www.docker.com/>
<https://docker.events.cube365.net/docker/dockercon/>
