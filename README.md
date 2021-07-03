# Robot-operating-system-installation-and-configuration

In this project, we want to create a robot arm, and to start we need to create a simulation of the robot arm using a robot operating system AKA “ROS”.

ROS can be either be installed on Ubuntu using Virtual Box or it can be found online using https://www.theconstructsim.com/, I chose to work with the online tool as working with ubuntu requires a lot of the PC space. However, by using the online tool you will notice some difficulties as it doesn’t support all the existing functions as ubuntu.

## Start a new project
After signing up at https://www.theconstructsim.com/, click on create a project and the following screen will appear. start filling the blanks by writing the project name, choose which ROS version you want to work with, and in my case I’m working with ROS Melodic, and finally add a brief description then click create.

![](arduino_robot_arm.png)

## installing the package (arduino_robot_arm)
The next step is to clone the robot arm package from GitHub, so we will use the command (Sudo apt install git) to install Github on ROS to clone the project using its' path from GitHub to ROS.

![](arduino_robot_arm.png)

## Install all the dependencies 
To run the package we need other dependencies (MoveIt, joint state publisher, gazebo ..etc), so we used the following commands to install those dependencies on ROS, and we complied the package after the installation is completed.

![](arduino_robot_arm.png)
![](arduino_robot_arm.png)

## Controlling the motors
Now we run the robot arm package using the following command (roslaunch robot_arm_pkg check_motors.launch) which will result in two separate windows, where RVis window will show the arm structure simulation and the other is the joint state publisher window showing 4 controls to adjust the positioning of the parts.

![](arduino_robot_arm.png)

## Controlling the motors in simulation
using the following commands, now we will run the arm simulation on both RVis and Gazebo and adjust the arm using the controls.
$ roslaunch robot_arm_pkg check_motors.launch
$ roslaunch robot_arm_pkg check_motors_gazebo.launch
$ rosrun robot_arm_pkg joint_states_to_gazebo.py

which will result in the following windows:
![](arduino_robot_arm.png)

## MoveIt in RVis
To define the positioning of the arm and its' movements we use MoveIt which simulates the arm movement in different directions and scenarios (facing obstacles or not) and we can run it using the command (roslaunch moveit_pkg demo.launch) which will result in the following window:

![](arduino_robot_arm.png)
