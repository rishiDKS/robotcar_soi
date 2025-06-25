# 1. URDF Visualization in RViz

This repository contains URDF files to model and visualize a custom 3D robot in ROS using RViz.

# 2. Driving Virtual bot

Simulating robot moving in gazebo by keyboard


## Commands
```
source install/setup.bash
colcon build --symlink-install

ros2 launch robotcar rsp.launch.py
```

```
rviz2

ros2 run joint_state_publisher_gui joint_state_publisher_gui


rviz2 -d src/robotcar/config/robotcar.rviz
```
---

## simtime in gazebo
launch_sim.launch.py code:
```
ros2 launch robotcar rsp.launch.py use_sim_time:=true


ros2 launch gazebo_ros gazebo.launch.py


ros2 run gazebo_ros spawn_entity.py -topic robot_description -entity bot_name

```
```
ros2 launch robotcar launch_sim.launch.py

```
teleop_twist_keyboard
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```
for debugging
```
ros2 topic echo /cmd_vel   
```
run from saved world:
```
ros2 launch robotcar launch_sim.launch.py world:=src/robotcar/worlds/obstacles.world

```
## commit-4:

added lidar : lidar.xacro file

## commit-5:
added camera : camera.xacro

can't get compressed images
```
sudo apt install ros-humble-image-transport-plugins

source /opt/ros/humble/setup.bash

sudo apt install ros-humble-rqt-image-view

ros2 run rqt_image_view rqt_image_view

```
## commit-6:
added depth camera : depth_camera.xacro
<!-- ## 📁 Project Structure -->

