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

