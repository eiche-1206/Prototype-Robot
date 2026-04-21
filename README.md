# Autonomous Inspection Robot Based on ROS 2 and Navigation 2

## 1. Project Overview

This project implements an autonomous inspection robot simulation based on ROS 2 and Navigation 2. 

The repository is organized into the following packages:

| Package | Description |
|---|---|
| `fishbot_description` | Robot description files including simulation-related configurations |
| `fishbot_navigation2` | Robot navigation configuration files |
| `fishbot_application` | Python application code for robot navigation |

---

## 2. Usage

The development environment for this project is as follows:

- **OS:** Ubuntu 20.04
- **ROS Version:** ROS 2 Galactic

### 2.1 Installation

This project uses `slam-toolbox` for mapping, Navigation 2 for navigation, Gazebo for simulation, and `ros2-control` for motion control. Please install the required dependencies before building.

**1. Install SLAM and Navigation 2**
```shell
sudo apt install ros-$ROS_DISTRO-nav2-bringup ros-$ROS_DISTRO-slam-toolbox
```

**2. Install simulation-related packages**
```shell
sudo apt install ros-$ROS_DISTRO-robot-state-publisher \
                 ros-$ROS_DISTRO-joint-state-publisher \
                 ros-$ROS_DISTRO-gazebo-ros-pkgs \
                 ros-$ROS_DISTRO-ros2-controllers \
                 ros-$ROS_DISTRO-xacro
```

**3. Install text-to-speech and image-related packages**
```shell
sudo apt install python3-pip -y
sudo apt install espeak-ng -y
sudo pip3 install espeakng
sudo apt install ros-$ROS_DISTRO-tf-transformations
sudo pip3 install transforms3d
```

### 2.2 Running

Once all dependencies are installed, use `colcon` to build and run the project.

**Build all packages**
```shell
colcon build
```

**Launch simulation**
```shell
source install/setup.bash
ros2 launch fishbot_description gazebo_sim.launch.py
```

**Launch navigation**
```shell
source install/setup.bash
ros2 launch fishbot_navigation2 navigation2.launch.py
```

---

## 3. Author

- [Eiche](https://gitee.com/eiche1206)
## 基于 ROS 2 和 Navigation 2 自动巡检机器人

## 1.项目介绍

本项目基于 ROS 2 和  Navigation 2 设计了一个自动巡检机器人仿真功能。

各功能包功能如下：
- fishbot_description 机器人描述文件，包含仿真相关配置
- fishbot_navigation2 机器人导航配置文件
- fishbot_application 机器人导航应用 Python 代码

## 2.使用方法

本项目开发平台信息如下：

- 系统版本： Ubunt20.04
- ROS 版本：ROS 2 galactic

### 2.1安装

本项目建图采用 slam-toolbox，导航采用 Navigation 2 ,仿真采用 Gazebo，运动控制采用 ros2-control 实现，构建之前请先安装依赖，指令如下：

1. 安装 SLAM 和 Navigation 2

```shell
sudo apt install ros-$ROS_DISTRO-nav2-bringup ros-$ROS_DISTRO-slam-toolbox
```

2. 安装仿真相关功能包

```shell
sudo apt install ros-$ROS_DISTRO-robot-state-publisher  ros-$ROS_DISTRO-joint-state-publisher ros-$ROS_DISTRO-gazebo-ros-pkgs ros-$ROS_DISTRO-ros2-controllers ros-$ROS_DISTRO-xacro
```

3. 安装语音合成和图像相关功能包

```
sudo apt install python3-pip  -y
sudo apt install espeak-ng -y
sudo pip3 install espeakng
sudo apt install ros-$ROS_DISTRO-tf-transformations
sudo pip3 install transforms3d
```

### 2.2运行

安装完成依赖后，可以使用 colcon 工具进行构建和运行。

构建功能包

```
colcon build
```

运行仿真

```
source install/setup.bash
ros2 launch fishbot_description gazebo_sim.launch.py
```

运行导航

```
source install/setup.bash
ros2 launch fishbot_navigation2 navigation2.launch.py
```


## 3.作者

- [Eiche](https://gitee.com/eiche1206)
