# ENPM808X Turtlebot-walker-algorithm
## Overview of the project

For this assignment we had to implement a simple walker algorithm in which the 
robot should move forward until it reaches an obstacle, then rotate in place until 
the way ahead is clear then move forward again and repeat the process.

## Dependencies
[![ROS Kinetic Installation](https://img.shields.io/badge/ROSKinetic-Clickhere-brightgreen.svg?style=flat)](http://wiki.ros.org/kinetic/Installation)

## Standard install via command line
```
cd ~/catkin_ws/src
git clone --recursive https://github.com/bshantam97/turtlebot_walker_algorithm.git
cd ..
catkin_make 
```
### Installation of Turtlebot simulation stack type
```
 sudo apt-get install ros-kinetic-turtlebot-gazebo
 ros-kinetic-turtlebot-apps ros-kinetic-turtlebot-rviz-launchers
```

## Launch a simple turtlebot gazebo world
```
roslaunch turtlebot_gazebo turtlebot_world.launch
```

## Steps to run the program
Now open 2 terminals in catkin_ws

### Terminal 1
```
roscore
```
### Terminal 2(To enable/disable the rosbag recording)
```
source ./devel/setup.bash
roslaunch turtlebot_walker_algorithm turtlebot.launch record:=enable
```
If you dont want to record the bag file set record:=disable
```
source ./devel/setup.bash
roslaunch turtlebot_walker_algorithm turtlebot.launch record:=disable
```
## Steps to run the program using rosrun 
Open 3 terminals and follow the steps 

### Terminal 1
```
roscore
```
### Terminal 2
```
source ./devel/setup.bash
roslaunch turtlebot_gazebo turtlebot_world.launch
```
### Terminal 3
```
source ./devel/setup.bash
rosrun turtlebot_walker_algorithm walker
```
## Inspecting bag file and playing back .bag file
### To inspect the bag file use the following command
```
cd ~/catkin_ws/src/turtlebot_walker_algorithm/Results
rosbag info turtlebot_walker_algorithm.bag
```
### To play the bag file recording 
```
cd ~/catkin_ws/src/turtlebot_walker_algorithm/Results
rosbag play turtlebot_walker_algorithm.bag
```
