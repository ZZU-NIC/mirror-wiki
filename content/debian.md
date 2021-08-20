---
title: Debian
---
<!-- ex_nolevel -->
# Debian 镜像使用帮助

## 文档修订日期

2021-05-28

## 地址

http://mirrors.zzu.edu.cn/debian/

## 说明

Debian 软件源

## 收录架构

Debian 支持的所有架构，如 AMD64 (x86_64), Intel x86, ARM, MIPS, ppc64el, s390x 等

## 收录版本

Debian Old Stable, Stable, Testing, Unstable(sid)

当前 Stable 为 Debian 10，代号为 Buster

## 使用说明

> [!DANGER]
> 请注意备份原始文件


### 一键替换

一般情况下，将 /etc/apt/sources.list 文件中 Debian 默认的源地址 http://deb.debian.org/ 替换为 http://mirrors.zzu.edu.cn 即可。 可以使用如下命令：

```shell
sudo sed -i 's/deb.debian.org/mirrors.zzu.edu.cn/g' /etc/apt/sources.list
```

### 手工修改

当然也可以直接编辑 `/etc/apt/sources.list` 文件（需要使用 sudo）。以下是 Debian Stable 参考配置内容：

```
deb http://mirrors.zzu.edu.cn/debian stable main contrib non-free
# deb-src http://mirrors.zzu.edu.cn/debian stable main contrib non-free
deb http://mirrors.zzu.edu.cn/debian stable-updates main contrib non-free
# deb-src http://mirrors.zzu.edu.cn/debian stable-updates main contrib non-free

# deb http://mirrors.zzu.edu.cn/debian stable-proposed-updates main contrib non-free
# deb-src http://mirrors.zzu.edu.cn/debian stable-proposed-updates main contrib non-free
```

