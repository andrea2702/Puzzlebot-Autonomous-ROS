# Puzzlebot Autonomous Control with ROS

## Overview
This project focuses on creating an autonomous puzzle-solving robot using ROS (Robot Operating System). The robot is equipped with capabilities for traffic sign detection, traffic light detection, line following control, and decision-making using state machines. It utilizes NVIDIA Jetson for processing and YOLOv5 for traffic sign detection.

## Prerequisites
Before running this project, ensure you have the following prerequisites installed:
- ROS (Robot Operating System)
- Ubuntu 18.04 or 20.04
- Python libraries: NumPy, OpenCV, cv-bridge
- Time module (usually included in Python standard library)

## Workspace Packages
This ROS workspace includes the following packages:
1. **puzzlebot_autostart**: Manages the startup sequence for the puzzlebot.
2. **vehicle_control**: Handles control algorithms for the puzzlebot, including line following and response to traffic signs.
3. **yolo_rec**: Contains the YOLOv5 package for traffic sign detection.

## Launch Files
1. **puzzlebot_autostart.launch**: Launches the startup sequence for the puzzlebot.
2. **vehicle_control.launch**: Launches control algorithms for the puzzlebot.

## Features
- **Traffic Sign Detection**: Utilizes a Convolutional Neural Network (CNN) implemented in the YOLOv5 package for real-time detection of traffic signs on the track.
- **Traffic Light Detection**: Employs traditional computer vision techniques for detecting traffic lights.
- **Line Following Control**: Utilizes a Proportional-Integral (PI) controller to maintain the puzzlebot's alignment with the track's centerline.
- **Decision Making with State Machines**: Implements a state machine to make decisions based on detected traffic signs and lights.

## Usage
1. Clone this repository into your ROS workspace's `src` directory.
2. Navigate to your ROS workspace and build the packages:
   ```bash
   cd path/to/your/ros/workspace
   catkin_make
3. Source the setup script:
```bash
source devel/setup.bash
```
4. Launch the puzzlebot startup sequence:
```bash
roslaunch puzzlebot_autostart puzzlebot_autostart.launch
```
5. Launch the vehicle control:
``` bash
roslaunch vehicle_control vehicle_control.launch
```

## Demo
[![Demo del Proyecto](http://img.youtube.com/vi/bmP49zlKMyg/0.jpg)](https://www.youtube.com/watch?v=bmP49zlKMyg)
