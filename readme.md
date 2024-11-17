# TurtleBot3 SLAM Gmapping Launch File

This repository contains a ROS launch file for setting up SLAM (Simultaneous Localization and Mapping) on a TurtleBot3 using the Gmapping package.

## How to Use

Move the launch file to your TurtleBot3 SLAM package:
- Command: `cp turtlebot3_slam_gmapping.launch ~/catkin_ws/src/turtlebot3/turtlebot3_slam/launch/`

Build your workspace:
- Command: `cd ~/catkin_ws`
- Command: `catkin_make`

Launch the SLAM node:
- Command: `roslaunch turtlebot3_slam turtlebot3_slam_gmapping.launch`

## Parameters

The following are key parameters included in the launch file:

| Parameter             | Default Value | Description                                         |
|-----------------------|---------------|-----------------------------------------------------|
| `map_update_interval` | `2.0`         | Map update interval (seconds).                      |
| `maxUrange`           | `4.0`         | Maximum laser sensor range (meters).                |
| `particles`           | `120`         | Number of particles for the particle filter.        |
| `xmin`, `ymin`, `xmax`, `ymax` | `-10.0`, `-10.0`, `10.0`, `10.0` | Initial map dimensions (meters).  |
| `linearUpdate`        | `0.2`         | Minimum travel distance for map updates.            |
| `angularUpdate`       | `0.2`         | Minimum rotation for map updates.                   |

## Prerequisites

Ensure the following prerequisites are installed and configured:

1. **Robot Operating System (ROS)**:
   - Recommended: ROS Noetic for Ubuntu 20.04.

2. **TurtleBot3**:
   - Properly set up and configured with a LiDAR sensor.

3. **Dependent ROS Packages**:
   - Install the `gmapping` package:
     - Command: `sudo apt-get install ros-noetic-slam-gmapping`


