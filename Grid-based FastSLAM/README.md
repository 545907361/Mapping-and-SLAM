# ROS-SLAM
## 使用开源turtlebot机器人建图
首先，克隆gmapping软件包，安装其系统依赖项，并构建catkin工作区
``` bash
$ cd /catkin_ws/src
$ git clone https://github.com/ros-perception/slam_gmapping
$ rosdep install gmapping
$ cd..
$ catkin_make
```
终端1 在环境中启动乌龟机器人
``` bash
$ cd /home/workspace/catkin_ws
$ source devel/setup.bash
$ roslaunch turtlebot_gazebo turtlebot_world.launch world_file:=worlds/willowgarage.world 
```
终端2 启动键盘伸缩节点
``` bash
$ cd /home/workspace/catkin_ws
$ source devel/setup.bash
$ roslaunch turtlebot_teleop keyboard_teleop.launch
```
终端3 运行slam_gmapping节点
``` bash
$ cd /home/workspace/catkin_ws
$ source devel/setup.bash
$ rosrun gmapping slam_gmapping
```
终端4 运行rviz并订阅不同的已发布主题以可视化地图
``` bash
$ rosrun rviz rviz
```
终端5 保存环境图
``` bash
$ cd /catkin_ws/src
$ rosrun map_server map_saver -f myMap
```
