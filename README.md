# LIO-SAM

For details, see the [original repository](https://github.com/TixiaoShan/LIO-SAM)

## Dependency

- [ROS](http://wiki.ros.org/ROS/Installation)
  ```bash
  sudo apt-get install -y ros-noetic-navigation
  sudo apt-get install -y ros-noetic-robot-localization
  sudo apt-get install -y ros-noetic-robot-state-publisher
  ```
- [gtsam](https://gtsam.org/get_started/)
  ```bash
  sudo add-apt-repository ppa:borglab/gtsam-release-4.2
  sudo apt-get update
  sudo apt-get install libgtsam-dev libgtsam-unstable-dev
  ```

## Install

Use the following commands to download and compile the package:
```bash
cd ~/catkin_ws/src
git clone https://github.com/adthoms/LIO-SAM
cd ..
catkin build
```

## Run the package

1. Run the launch file:
```bash
roslaunch lio_sam run.launch
```

2. Play existing bag files:
```bash
rosbag play your_bag.bag --pause
```

## Service

Save map as a PCD file via:
``` bash
rosservice call [service] [resolution] [destination]
```

Example:
``` bash
rosservice call /lio_sam/save_map 0.2 "/Downloads/LOAM/"
```
