---
title: Arch Linux ARM
---
# Arch Linux ARM 镜像使用帮助

## 文档修订日期

2021-04-28

## 地址

http://mirrors.zzu.edu.cn/archlinuxarm/

## 说明

Arch Linux ARM 软件源

## 收录架构

ARMv5, ARMv6, ARMv7, AArch64

## 使用说明

编辑`/etc/pacman.d/mirrorlist`，先注释掉里面的所有行，然后在文件的最顶端添加

```
Server = http://mirrors.zzu.edu.cn/archlinuxarm/$repo/os/$arch
```

更新软件包缓存：

```
sudo pacman -Syy
```

## 相关链接

- 官方主页：https://www.archlinuxarm.org/
- 论坛：https://archlinuxarm.org/forum/
- Wiki：https://archlinuxarm.org/wiki