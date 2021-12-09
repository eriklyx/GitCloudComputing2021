#### Docker安装

先根据以下代码安装curl

```
sudo apt-get update
sudo apt-get install 
```

添加使用HTTPS传输的软件包以及CA证书

```
sudo apt-get update
sudo apt-get install
```

向source.list中添加Docker软件源

```
sudo add-apt-repository
(lsb_release -cs)
```

更新apt软件包缓存，并安装Docker-ce

```
sudo apt-get update
sudo apt-get install docker-ce
```

测试Docker是否安装正确

```
docker run hello-world
```

查看Docker版本

```
docker –version
docker-compose –version
```

```
#Docker version 20.10.8, build 3967b7d
#compose version 1.29.2, build 5becea4c
```

#### Docker运行第一个容器

```
docker run hello-world
```

```
# Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```

#### 查看当前正在运行或过去运行的所有容器

```
docker ps -a
```

```
#CONTAINER ID   IMAGE         COMMAND    CREATED         STATUS                     PORTS     NAMES
639f2f5253f4   hello-world   "/hello"   2 minutes ago   Exited (0) 2 minutes ago             practical_dubinsky
0c34dc38e60c   hello-world   "/hello"   2 weeks ago     Exited (0) 2 weeks ago               adoring_bose

```

#### 创建Docker镜像

使用niginx镜像启动容器

```
docker container run --rm --detach --name default-nginx --publish 8080:80 nginx
```

```
#Unable to find image 'nginx:latest' locally
latest: Pulling from library/nginx
7d63c13d9b9b: Pull complete 
15641ef07d80: Pull complete 
392f7fc44052: Pull complete 
8765c7b04ad8: Pull complete 
8ddffa52b5c7: Pull complete 
353f1054328a: Pull complete 
Digest: sha256:dfef797ddddfc01645503cef9036369f03ae920cac82d344d58b637ee861fda1
Status: Downloaded newer image for nginx:latest
2e26f3cd1fdd41b2c50186c9de13fe66861502721540d2658e0728372f02e173
```

