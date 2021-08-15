---
title: CTAN
---
<!-- ex_nolevel -->
# CTAN 镜像使用帮助

## 文档修订日期

2021-04-14

## 地址

http://mirrors.zzu.edu.cn/ctan

## 使用说明

[CTAN](https://www.ctan.org/) (The Comprehensive TeX Archive Network) 镜像源可以使用 TeX Live 管理器 tlmgr 更改。

在命令行中执行

```
tlmgr option repository http://mirrors.zzu.edu.cn/CTAN/systems/texlive/tlnet
```

即可永久更改镜像源。

如果只需要临时切换，可以用如下命令：

```
tlmgr update --all --repository http://mirrors.zzu.edu.cn/CTAN/systems/texlive/tlnet
```

其中的 **update --all** 指令可根据需要修改。