# 服务器

在网站的服务器上，你也需要去安装 Docker。服务器的操作系统一般都是 Linux 类型的，比如 Ubuntu，Debian，CentOS，Fedora 等等，你要选择跟自己的服务器操作系统对应的 Docker 去安装一下。我的服务器都是 CentOS 系统，所以推荐大家也用这种操作系统作为你的网站服务器的操作系统。

## CentOS

需要用 64 位的 CentOS 7，如果系统里安装过以前版本的 Docker，可以先删除掉它们，旧版的 Docker 叫 docker 或 docker-engine，用 yum 可以先试着删除掉它们。

```
sudo yum remove docker docker-common container-selinux docker-selinux docker-engine
```

安装



