---
title: Ubuntu
---
# Ubuntu 镜像使用帮助

## 文档修订日期

2021-05-28

## 收录架构

- ALL

## 收录版本

- ALL

## 使用说明

### 手动更改配置文件

警告：操作前请做好相应备份

#### 一键替换

一般情况下，将 /etc/apt/sources.list 文件中 Ubuntu 默认的源地址 http://deb.debian.org/ 替换为 http://mirrors.zzu.edu.cn 即可。 可以使用如下命令：

```shell
sudo sed -i 's/archive.ubuntu.com/mirrors.zzu.edu.cn/g' /etc/apt/sources.list
```

**小技巧**

1. Ubuntu 图形安装器会根据用户设定的时区推断 locale，这导致默认的源地址通常不是 `http://archive.ubuntu.com/`， 而是 `http://<country-code>.archive.ubuntu.com/ubuntu/` ，如 `http://cn.archive.ubuntu.com/ubuntu/`， 此时只需将上面的命令进行相应的替换即可，即 `sudo sed -i 's/cn.archive.ubuntu.com/mirrors.zzu.edu.cn/g' /etc/apt/sources.list`。

2. 因镜像站同步有延迟，可能会导致生产环境系统不能及时检查、安装上最新的安全更新，不建议替换 security 源。 如果有官方源下载速度不理想等问题，想通过镜像站下载安全更新， 可以将 security 源地址从 `http://security.ubuntu.com/` 替换为 `http://mirrors.zzu.edu.cn/`，即 `sudo sed -i 's/security.ubuntu.com/mirrors.zzu.edu.cn/g' /etc/apt/sources.list`。

#### 手工修改

当然也可以直接编辑 `/etc/apt/sources.list` 文件（需要使用 sudo）。以下是 Ubuntu 20.04 参考配置内容：

```
# 默认注释了源码仓库，如有需要可自行取消注释
deb https://mirrors.zzu.edu.cn/ubuntu/ focal main restricted universe multiverse
# deb-src https://mirrors.zzu.edu.cn/ubuntu/ focal main restricted universe multiverse

deb https://mirrors.zzu.edu.cn/ubuntu/ focal-security main restricted universe multiverse
# deb-src https://mirrors.zzu.edu.cn/ubuntu/ focal-security main restricted universe multiverse

deb https://mirrors.zzu.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
# deb-src https://mirrors.zzu.edu.cn/ubuntu/ focal-updates main restricted universe multiverse

deb https://mirrors.zzu.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
# deb-src https://mirrors.zzu.edu.cn/ubuntu/ focal-backports main restricted universe multiverse

# 预发布软件源，不建议启用
# deb https://mirrors.zzu.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
# deb-src https://mirrors.zzu.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
```

更改完 `sources.list` 文件后请运行 `sudo apt-get update` 更新索引以生效。

如要用于其他版本，把 **focal** 换成其他版本代号即可: 20.04：`focal`；18.04：`bionic`；16.04：`xenial`；14.04：`trusty`。

### 镜像下载

如果需要下载 Ubuntu 的 ISO 镜像以便安装，请访问 [镜像站主页](http://mirrors.zzu.edu.cn)

