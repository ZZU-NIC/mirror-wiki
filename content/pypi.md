# PyPI 镜像源使用帮助

## 文档修订日期

2021-04-23

## 地址

http://pypi.mirrors.zzu.edu.cn/simple

## 说明

PyPI(Python Package Index)是python官方的第三方库的仓库，所有人都可以下载第三方库或上传自己开发的库到PyPI。PyPI推荐使用pip包管理器来下载第三方库。本站提供 Pypi 的反向代理镜像，以加快校内访问速度。

## 使用说明

### 临时使用

```shell
pip install -i http://pypi.mirrors.zzu.edu.cn/simple some-packet --trusted-host pypi.mirrors.zzu.edu.cn
```

### 设为默认

升级 `pip` 到最新的版本 `(>=10.0.0)` 后进行配置：

```shell
pip install -i http://pypi.mirrors.zzu.edu.cn/simple pip -U --trusted-host pypi.mirrors.zzu.edu.cn
pip config set global.index-url http://pypi.mirrors.zzu.edu.cn/simple
pip config set install.trusted-host pypi.mirrors.zzu.edu.cn
```

## 同步方式

- 反向代理 + 缓存（Devpi）
- 上游：mirrors.bfsu.edu.cn

## 相关链接

- pip：https://pip.pypa.io/
- bandersnatch：https://pypi.python.org/pypi/bandersnatch