---
title: Kubernetes
---
# Kubernetes 镜像使用帮助

## 地址

https://mirrors.ustc.edu.cn/kubernetes/

## 说明

Kubernetes 是用于自动部署，扩展和管理容器化应用程序的开源系统。详情可见 [官方介绍](https://kubernetes.io/zh/)。

**硬件架构: `x86_64`, `armhfp`, `aarch64`**

### Debian/Ubuntu 用户

首先导入 gpg key：

```
$ curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
```

新建 `/etc/apt/sources.list.d/kubernetes.list`，内容为

```
# Ubuntu 14.04 LTS
deb http://mirrors.zzu.edu.cn/kubernetes/apt kubernetes-trusty main
# Ubuntu 16.04 LTS
deb http://mirrors.zzu.edu.cn/kubernetes/apt kubernetes-xenial main
# Debian 8 (Jessie)
deb http://mirrors.zzu.edu.cn/kubernetes/apt kubernetes-jessie main
# Debian 9 (Stretch) 
deb http://mirrors.zzu.edu.cn/kubernetes/apt kubernetes-stretch main
```

### RHEL/CentOS 用户

新建 `/etc/yum.repos.d/kubernetes.repo`，内容为：

```
[kubernetes]
name=kubernetes
baseurl=http://mirrors.zzu.edu.cn/kubernetes/yum/repos/kubernetes-el7-$basearch
enabled=1
```

### Minikube

请到 [minikube 镜像](http://mirrors.zzu.edu.cn/github-release/kubernetes/minikube/LatestRelease/) 下载。