---
title: Kali
---
<!-- ex_nolevel -->
# Kali 镜像使用帮助

## 文档修订日期

2021-05-15

## 地址

http://mirrors.zzu.edu.cn/kali/

## 说明

Kali Linux 软件源

## 支持的系统架构

amd64, armel, armhf, i386

## 使用说明

编辑 /etc/apt/sources.list 文件, 在文件最前面添加以下条目：

```shell
deb http://mirrors.zzu.edu.cn/kali kali-rolling main non-free contrib
deb-src http://mirrors.zzu.edu.cn/kali kali-rolling main non-free contrib
```

更改完 **sources.list** 文件后请运行 **sudo apt-get update** 更新索引以生效。

## 相关链接

- 官方主页： https://www.kali.org/
- 论坛： http://forums.kali.org/
- 文档： https://www.kali.org/kali-linux-documentation/