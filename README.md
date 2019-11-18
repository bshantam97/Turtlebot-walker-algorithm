# ENPM808X Turtlebot-walker-algorithm
## Overview of the project

For this assignment we had to implement a simple walker algorithm in which the 
robot should move forward until it reaches an obstacle, then rotate in place until 
the way ahead is clear then move forward again and repeat the process.

## Dependencies
[![ROS Kinetic Installation](https://img.shields.io/badge/ROSKinetic-Clickhere-brightgreen.svg?style=flat)](http://wiki.ros.org/kinetic/Installation)

### Installation of Turtlebot simulation stack type
```
 sudo apt-get install ros-kinetic-turtlebot-gazebo
 ros-kinetic-turtlebot-apps ros-kinetic-turtlebot-rviz-launchers
```

## Launch a simple turtlebot gazebo world
```
roslaunch turtlebot_gazebo turtlebot_world.launch
``
