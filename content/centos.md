---
title: CentOS
---
<!-- ex_nolevel -->
# CentOS 镜像使用帮助

## 文档修订日期

2021-04-28：由于上级源取消旧版本支持，本站CentOS镜像源同步变更，敬请谅解。

## 地址

http://mirrors.zzu.edu.cn/centos/

## 说明

CentOS 软件源

## 收录架构

x86_64, i386

## 收录版本

7, 8

## 使用说明

> [!WARNING]
> 请注意备份原始文件

1. 备份/etc/yum.repos.d/内文件

   CentOS 7 及之前为 CentOS-Base.repo，CentOS 8 为CentOS-Linux-*.repo

2. 编辑 /etc/yum.repos.d/ 中的相应文件，在 mirrorlist= 开头行前面加 # 注释掉；并将 baseurl= 开头行取消注释（如果被注释的话），把该行内的域名（例如http://mirror.centos.org）替换为 http://mirrors.zzu.edu.cn。

如为默认源，以上步骤可通过下方命令一键完成
CentOS 7：

```shell
sudo sed -e 's|^mirrorlist=|#mirrorlist=|g' \
	-e 's|^#baseurl=http://mirror.centos.org|baseurl=http://mirrors.zzu.edu.cn|g' \
	-i.bak \
	/etc/yum.repos.d/CentOS-Base.repo
```

CentOS 8：

```shell
sudo sed -e 's|^mirrorlist=|#mirrorlist=|g' \
	-e 's|^#baseurl=http://mirror.centos.org|baseurl=http://mirrors.zzu.edu.cn|g' \
	-i.bak \
	/etc/yum.repos.d/CentOS-Linux-AppStream.repo \
	/etc/yum.repos.d/CentOS-Linux-BaseOS.repo \
	/etc/yum.repos.d/CentOS-Linux-Extras.repo \
	/etc/yum.repos.d/CentOS-Linux-PowerTools.repo \
	/etc/yum.repos.d/CentOS-Linux-Plus.repo
```

如非默认源，您可以选择下载以下文件，并手动替换原文件

CentOS 8

* [CentOS-Linux-AppStream.repo](http://mirrors.zzu.edu.cn/wiki/centos/download/8/CentOS-Linux-AppStream.repo)
* [CentOS-Linux-BaseOS.repo](http://mirrors.zzu.edu.cn/wiki/centos/download/8/CentOS-Linux-BaseOS.repo)
* [CentOS-Linux-Extras.repo](http://mirrors.zzu.edu.cn/wiki/centos/download/8/CentOS-Linux-Extras.repo)
* [CentOS-Linux-PowerTools.repo](http://mirrors.zzu.edu.cn/wiki/centos/download/8/CentOS-Linux-PowerTools.repo)
* [CentOS-Linux-Plus.repo](http://mirrors.zzu.edu.cn/wiki/centos/download/8/CentOS-Linux-Plus.repo)

CentOS 7

* [CentOS-Base.repo](http://mirrors.zzu.edu.cn/wiki/centos/download/7/CentOS-Base.repo)

3. 运行以下命令，更新软件包缓存

```shell
yum clean all
yum makecache
```

## 相关链接

- 官方主页：https://www.centos.org/
- 邮件列表：https://wiki.centos.org/zh/GettingHelp/ListInfo
- 论坛：https://forums.centos.org/
- 文档：https://docs.centos.org/
- Wiki：https://wiki.centos.org/zh/
- 镜像列表：https://www.centos.org/download/mirrors/

