---
title: Arch Linux
---
<!-- ex_nolevel -->
# Arch Linux 镜像使用帮助

## 文档修订日期

2021-04-28

## 地址

http://mirrors.zzu.edu.cn/archlinux/

## 说明

Arch Linux 软件源

## 收录架构

i686, x86_64

## 收录版本

- ALL

## 使用说明

编辑`/etc/pacman.d/mirrorlist`，先注释掉里面的所有行，然后在文件的最顶端添加

```shell
Server = http://mirrors.zzu.edu.cn/archlinux/$repo/os/$arch
```

## 相关链接

- 官方主页：https://www.archlinux.org/
- 邮件列表：https://www.archlinux.org/mailman/listinfo/
- 论坛：https://bbs.archlinux.org/
- Wiki：https://wiki.archlinux.org/

