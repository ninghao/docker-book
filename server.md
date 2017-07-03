# 服务器

在网站的服务器上，你也需要去安装 Docker。服务器的操作系统一般都是 Linux 类型的，比如 Ubuntu，Debian，CentOS，Fedora 等等，你要选择跟自己的服务器操作系统对应的 Docker 去安装一下。我的服务器都是 CentOS 系统，所以推荐大家也用这种操作系统作为你的网站服务器的操作系统。

## CentOS

需要用 64 位的 CentOS 7。你可以购买一台按量付费的 CentOS  7 系统的阿里云 ECS 服务器，在上面安装运行一个 Docker，测试完成以后，可以释放服务器，这样也花不了多少钱。或者你也可以在本地创建一台 CentOS 7 系统的虚拟机，然后在上面安装运行 Docker，这样不需要花一分钱就可以学习在 CentOS 系统上使用 Docker。

### 删除旧版

如果系统里安装过以前版本的 Docker，可以先删除掉它们，旧版的 Docker 叫 docker 或 docker-engine，用 yum 可以先试着删除掉它们。

```
sudo yum remove docker docker-common container-selinux docker-selinux docker-engine
```

### 配置仓库

先安装一些需要的包，yum-utils 提供了 yum-config-manager 工具，device-mapper-persistent-data 与 lvm2 是 devicemapper 存储引擎需要的包。

```
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
```

配置一下 Docker 稳定版的仓库，stable 参数是必须的，即使你打算用 edge 或 testing 版本的 Docker，也需要先有 stable 仓库才行。

```
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

如果你想用稳定版的 Docker，现在就可以去安装了。如果打算用 edge 或 testing 版的 Docker，你可以先配置一下：

```
sudo yum-config-manager --enable docker-ce-edge
```

```
sudo yum-config-manager --enable docker-ce-testing
```

禁用仓库，可以这样做：

```
sudo yum-config-manager --disable docker-ce-edge
```

### 安装 Docker

安装最新版的 Docker，执行：

```
sudo yum install docker-ce
```

查看可用版本：

```
yum list docker-ce.x86_64 --showduplicates | sort -r
```

安装指定版本的 Docker：

```
sudo yum install docker-ce-<VERSION>
```

### 启动 Docker

执行：

```
sudo systemctl start docker
sudo systemctl enable docker
```

验证一下：

```
sudo docker run hello-world
```

### 删除 Docker

执行：

```
sudo yum remove docker-ce
```

镜像，容器，数据卷都在 /var/lib/docker 下面，删除这些东西，执行：

```
sudo rm -rf /var/lib/docker
```



