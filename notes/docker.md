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

pull image from registry or download image from registry to local machine
```shell
$ docker pull nginx
```

### Docker System Information
```shell
$ sudo docker info
$ sudo docker --version
$ sudo docker version
$ docker version
$ docker --version
```
