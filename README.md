# Baxter Motion Planner
[![License](https://img.shields.io/badge/License-MIT%20-blue.svg)](https://github.com/urastogi885/baxter-motion-planner/blob/master/LICENSE)

## Overview
This projects simulates the pick and place ability of Baxter along with obstacle avoidance. The Rviz path planner was used to extract coordinates for the robot to follow a specific path. These points were finally fed to the [*ik_pick_and_place node*](https://github.com/urastogi885/baxter-motion-planner/blob/master/scripts/ik_pick_and_place_demo.py) to simulate baxter's motion in Gazebo.

## Dependencies

- ROS Kinetic
- Gazebo
- MoveIt
- Rviz
- Baxter Simulator

## Install Dependencies

- This project was developed using ROS Kinetic.
- It is highly recommended that ROS Kinetic is properly installed on your system before the use of this project.
- Follow the instructions on the [*ROS kinetic install tutorial page*](http://wiki.ros.org/kinetic/Installation/Ubuntu)
  to install ***Full-Desktop Version*** of ROS Kinetic.
  - If you have the *full-desktop* version of ROS, you can skip the next 2 steps.
- The full-version would help you install *Gazebo* as well. If you have ROS Kinetic pre-installed on your machine, use
  the following [*link*](http://gazebosim.org/tutorials?tut=install_ubuntu&cat=install) to just install *Gazebo* on your
  machine.
- Ensure successful installation by running *Gazebo* via your terminal window:

```
gazebo
```
- Install *moveit* using the following command:

```
sudo apt-get install ros-kinetic-moveit
```
- Install other packages for *move-it Rviz* interface:

```
cd ~/workspace/src
git clone https://github.com/ros-planning/moveit_robots.git
cd ..
catkin_make
```
- Create your ROS workspace by following instructions on the [*create ROS workspace tutortial page*](http://wiki.ros.org/catkin/Tutorials/create_a_workspace).
- Follow the [*Rethink Robotics link*](https://sdk.rethinkrobotics.com/wiki/Simulator_Installation) to setup the Baxter simulator.

## Build

Switch to your *src* sub-directory of your ROS workspace to clone this repository.
```
<ROS Workspace>/src
```
- Run the following commands to clone and build this project:
```
git clone --recursive https://github.com/urastogi885/Supermarket-Cleaning-Robot
cd ../
catkin_make
```

## Run

Now, we use launch file to run. In a new terminal, type:

```
cd catkin_ws
source devel/setup.bash
roslaunch baxter-motion-planning baxter.launch
```
