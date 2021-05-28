# ROS 源使用帮助

## 地址

http://mirrors.zzu.edu.cn/ros/

## 说明

机器人操作系统（ROS）的软件源镜像。

## 使用说明

### Ubuntu, Debian

1. 将软件源添加至系统:

   ```
   sudo sh -c 'echo "deb http://mirrors.zzu.edu.cn/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   ```

如果 IPv6 地址无效导致无法刷新软件源信息，将 `mirrors.zzu.edu.cn` 改成 `ipv4.mirrors.zzu.edu.cn` 以强制使用 IPv4。

1. 导入key:

   ```
   sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
   ```

2. 刷新软件源缓存 `sudo apt update`，安装所需的ros发行版。

## 相关链接

- 项目主页：http://www.ros.org/
