# Autonics LSC ROS Driver
This ROS Driver is for Autonics LSC-C Series

### Table of Contents

- [Supported Hardware](1.-supported-hardware)
- [ROS API](2.-ROS-API)
- [Build](3.-Build)
- [Start](4.-Start)


### 1. Supported Hardware
#### 1.1 Model name : LSC-C Series
#####   Website : [Autonics/LiDAR/LSC-C](https://www.autonics.com/series/3001018)


### 2. ROS API
#### 2.1 Published Topics
* scan(sensor_msgs/LaserScan) : Scan data from the device
* diagnostics(diagnostic_updater) : Scan topic status
#### 2.2. Services
* self_test(self_test::Testrunner) : checking communication connection
#### 2.3. Parameters
* addr(default : 192.168.0.1, type : string) - The device ip address
* port(default : 8000, type : int) - The port number of device
* frame_id(default : laser, type : string) - The frame name of scan data
* range_min(default : 0.05, type : double) - Minimum range value [m]
* range_max(default : 25.0, type : double) - Maximum range value [m]
* password(default : 0000, type : string) - Password to login LSC-C


### 3. Build
####   3.1 from source
    source /opt/ros/<rosdistro>/setup.bash
    makdir -p ~/catkin_ws/src/
    cd ~/catkin_ws/src/
    git clone https://github.com/autonicsDev/lsc_ros_driver.git
    cd ~/catkin_ws
    catkin_make


### 4. Start
    roslaunch lsc_ros_driver lsc_c25_launch.launch
