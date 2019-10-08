
# Where Am I?

![Image description](https://github.com/SEUlBI-hub/Udacity_Project3/blob/master/capture_localisation.JPG)

In this project, you will learn to utilize ROS packages to accurately localize a mobile robot inside a provided map in the Gazebo and RViz simulation environments.

Over the course of the project, as part of the Robotics Software Engineer Nanodegree, you will learn about several aspects of robotics with a focus on ROS, including -

- Building a mobile robot for simulated tasks.

- Creating a ROS package that launches a custom r-obot model in a Gazebo world and utilizes packages like AMCL and the Navigation Stack.

- Exploring, adding, and tuning specific parameters corresponding to each package to achieve the best possible localization results.

## Installation Instructions

The project can be complete in the provided Workspace in the Classroom. Alternatively, it can be completed on an Ubuntu System with ROS Kinetic installed on it. Some specific ROS packages might be required in order to complete the project -


``` bash
$ sudo apt-get install ros-kinetic-navigation
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-move-base
$ rospack profile
$ sudo apt-get install ros-kinetic-amcl
```

**Note:** We won't be able to provide support for native ROS installations, but you can post in the #ros channel in the ND Slack to start discussions with your fellow students if you face any issues.

## Required packages

1. AMCL Package
 The ROS AMCL package (http://wiki.ros.org/amcl) implements this variant and you will integrate this package with your robot to localize it inside the provided map.
 Here is the list of nodes required for AMCL package to operate
 - Map server node: name = "map_server"
 - AMCL node: name = "amcl"
 - Move base node: name = "move_base"
 
2. Teleop Package
$ cd /home/workspace/catkin_ws/src
$ git clone https://github.com/ros-teleop/teleop_twist_keyboard
$ cd ..
$ catkin_make
$ source devel/setup.bash

## Run the Project

After completing the project, you can launch it by running the following commands first -

```bash
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
```

And then run the following in *separate* terminals -

``` bash
$ roslaunch my_robot world.launch
$ roslaunch my_robot amcl.launch
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
