# 准备 Docker

Docker 在不同语境下带表不同的东西，一般指的是 Docker 引擎，有了这个引擎你才能在服务器上运行容器。Docker 引擎只能在 Linux 核心的系统上运行。Docker 公司也做了些工具，也可以让你在 Windows 或 macOS 上使用 Docker ，这些工具都用了一些虚拟化的技术，这是因为 Docker 引擎只能在 Linux 核心的系统上运行。这些工具在你的桌面设备上虚拟出了可以让 Docker 引擎运行的环境。

## 企业版与社区版

Docker EE（Docker Enterprise Edition）指的是企业版的 Docker，提供了更多的功能与服务，每年你需要付一定的费用。Docker CE（Docker Community Edition）指的是社区版的 Docker，你可以免费使用。一般我们只需要用社区版的 Docker 就行了，不用担心费用问题。

## 

## 服务器

在网站的服务器上，你也需要去安装 Docker。服务器的操作系统一般都是 Linux 类型的，比如 Ubuntu，Debian，CentOS，Fedora 等等，你要选择跟自己的服务器操作系统对应的 Docker 去安装一下。我的服务器都是 CentOS 系统，所以推荐大家也用这种操作系统作为你的网站服务器的操作系统。

### CentOS

需要用 64 位的 CentOS 7，如果系统里安装过以前版本的 Docker，可以先删除掉它们，旧版的 Docker 叫 docker 或 docker-engine，用 yum 可以先试着删除掉它们。

```
sudo yum remove docker docker-common container-selinux docker-selinux docker-engine
```

安装

