# ArchLinuxCN 镜像使用帮助

## 文档修订日期

2021-04-28

## 地址

http://mirrors.zzu.edu.cn/archlinuxcn/

## 简介

Arch Linux 中文社区仓库是由 Arch Linux 中文社区驱动的非官方用户仓库。包含中文用户常用软件、工具、字体/美化包等。

仓库地址：[http://repo.archlinuxcn.org](http://repo.archlinuxcn.org/)

## 使用说明

Arch Linux 中文社区仓库 是由 Arch Linux 中文社区驱动的非官方用户仓库。包含中文用户常用软件、工具、字体/美化包等。
完整的包信息列表（包名称/架构/维护者/状态）请 [点击这里](https://github.com/archlinuxcn/repo) 查看。

- 官方仓库地址：[https://repo.archlinuxcn.org](https://repo.archlinuxcn.org/)
- 镜像地址: http://mirrors.zzu.edu.cn/archlinuxcn/

使用方法：在 `/etc/pacman.conf` 文件末尾添加以下两行：

```
[archlinuxcn]
Server = http://mirrors.zzu.edu.cn/archlinuxcn/$arch
```

之后安装 archlinuxcn-keyring 包导入 GPG key。

## 相关链接

- Arch Linux 中文社区主页：[https://www.archlinuxcn.org](https://www.archlinuxcn.org/)
- Arch Linux 中文社区仓库 / 镜像加速源介绍：https://www.archlinuxcn.org/archlinux-cn-repo-and-mirror/

