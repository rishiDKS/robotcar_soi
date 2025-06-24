# URDF Visualization in RViz

This repository contains URDF (Unified Robot Description Format) files to model and visualize a custom robot in ROS using RViz.

---

## commands
```
source install/setup.bash

ros2 launch robotcar rsp.launch.py
```

```
rviz2

ros2 run joint_state_publisher_gui joint_state_publisher_gui

rviz2 -d src/robotcar/config/robotcar.rviz
```

---

## 📁 Project Structure

