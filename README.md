# RobotOne


RobotOne is a robot developed by Valkyrie UAV, this robot is created to be simulated in Gazebo and RViz

## Steps to create RobotOne based on ROS and Gazebo (Refazer)

### first step
RobotOne is based on Package the contains a C++ parser for the Unified Robot Description Format (URDF), which is an XML format for representing a robot model.

### RobotOne model is based on GuntherBot with differential drive
All components were created in the XML file with joints, collisions, pose, inertia and visual. The script file can be found here: [RobotOne description](https://github.com/LeonFS-code/robot_one/tree/master/robot_one_description). The files used in the RobotOne simulation are: [RobotOne Xacro](https://github.com/LeonFS-code/robot_one/blob/master/robot_one_description/urdf/robot_one.xacro) and [RobotOne Gazebo](https://github.com/LeonFS-code/robot_one/blob/master/robot_one_description/urdf/robot_one.gazebo).

## Steps clone and simulate this repository


1.Create a ROS Workspace (if you don't have yet)
```
mkdir -p ~/RobotOne_ws/src
cd RobotOne_ws
catkin init
cd src
git clone https://github.com/LeonFS-code/robot_one.git
cd RobotOne_ws
catkin_make
```

2.Start a simualtion

```
cd RobotOne_ws
source devel/setup.bash
roslaunch robot_one_gazebo robot_one_g1.launch
rosrun rviz rviz 
```