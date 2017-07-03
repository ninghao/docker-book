# 练习：理解镜像与容器

通过练习可以更好的理解镜像与容器。这个练习的所有操作都在本地电脑上完成，先启用你的 Docker for Windows 或 Docker for Mac。操作都是在命令行界面下完成，所以打开你的系统的命令行工具，Windows 用户可以使用 cmder，macOS 用户可以使用系统自带的终端工具。

## 下载镜像

后面我们会介绍自己构建镜像的方法，我们的镜像也需要基于某些镜像去构建。这里我们先去下载一个别人构建好的镜像，这就像是去下载一个软件，然后把它安装在自己的电脑上。

执行：

```
docker pull hello-world
```

`docker pull` 命令可以去下载在云上存储的镜像，上面我们下载了一个叫 hello-world 的镜像。

## 查看镜像列表

执行：

```
docker images
```

上面的命令会返回安装在系统上的镜像的列表。像这样：

```
REPOSITORY                                          TAG                 IMAGE ID            CREATED             SIZE
hello-world                                         latest              1815c82652c0        2 weeks ago         1.84kB
```

## 运行容器

执行：

```
docker run hello-world
```

`docker run` 这个命令可以基于镜像创建容器，上面的 hello-world 是镜像的名字，有些容器会一直运行，有些容器做完它要做的事以后就关掉了。运行上面的命令会返回：

```
Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://cloud.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/engine/userguide/
```

输出上面这些文字，就是基于 `hello-world` 这个镜像创建的容器要干的事儿。`hello-world` 这个镜像只是为了测试一下 Docker 。





