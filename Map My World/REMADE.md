# 使用RTAB-map构建地图 (RGBD相机)
## 安装依赖项，添加权限
```bash
$ sudo apt-get install ros-kinetic-rtabmap
$ sudo apt-get install ros-kinetic-rtabmap-ros
```
## 运行流程 
终端1 启动gazebo
```bash
$ roslaunch slam_project world.launch world_file:=~/catkin_ws/src/slam_project/worlds/kitchen_dining.world
```
终端2 启动Teleop节点
```bash
$ roslaunch slam_project teleop.launch
```
终端3 启动映射节点
```bash
$ roslaunch slam_project mapping.launch
```
终端4 启动Rviz
```bash
$ roslaunch slam_project rviz.launch
```
