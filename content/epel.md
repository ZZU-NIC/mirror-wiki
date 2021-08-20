---
title: EPEL
---
<!-- ex_nolevel -->
# EPEL 镜像使用帮助

## 文档修订日期

2021-04-28：优化脚本

## 地址

http://mirrors.zzu.edu.cn/epel/

## 说明

EPEL (Extra Packages for Enterprise Linux) 是由 Fedora Special Interest Group 为企业 Linux 创建、维护和管理的一个高质量附加包集合，适用于但不仅限于 Red Hat Enterprise Linux (RHEL), CentOS, Scientific Linux (SL), Oracle Linux (OL)。

## 收录架构

官方支持的所有架构

## 收录版本

官方支持的所有版本

## 使用说明

> [!WARNING]
> 请注意备份原始文件


### 1. 备份(如有配置其他epel源)

```shell
mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.backup
mv /etc/yum.repos.d/epel-testing.repo /etc/yum.repos.d/epel-testing.repo.backup
```

### 2. 执行以下命令：

```shell
sudo yum install -y epel-release
sudo sed -e 's|^metalink=|#metalink=|g' \
	-e 's|^#baseurl=https\?://download.fedoraproject.org/pub/epel/|baseurl=http://mirrors.zzu.edu.cn/epel/|g' \
	-i.bak \
	/etc/yum.repos.d/epel.repo
```

### 3. 如已替换过EPEL镜像源，可通过以下步骤手动部署

#### **epel(RHEL 8)**

1）安装 epel 配置包

```shell
yum install -y http://mirrors.zzu.edu.cn/epel/epel-release-latest-8.noarch.rpm
```

2）将 repo 配置中的地址替换为ZZU Mirrors镜像站地址

```shell
sed -i 's|^#baseurl=http://download.fedoraproject.org/pub|baseurl=http://mirrors.zzu.edu.cn|' /etc/yum.repos.d/epel*
sed -i 's|^metalink|#metalink|' /etc/yum.repos.d/epel*
```

#### **epel(RHEL 7)**

```shell
wget -O /etc/yum.repos.d/epel.repo http://mirrors.zzu.edu.cn/wiki/epel/download/epel-7.repo
```

#### **epel(RHEL 6)**

```shell
wget -O /etc/yum.repos.d/epel.repo http://mirrors.zzu.edu.cn/wiki/epel/download/epel-6.repo
```

#### **epel(RHEL 5)**

```shell
wget -O /etc/yum.repos.d/epel.repo http://mirrors.zzu.edu.cn/wiki/epel/download/epel-5.repo
```

## 相关链接

- 官方主页: https://fedoraproject.org/wiki/EPEL
- 镜像地址: http://mirrors.zzu.edu.cn/epel/