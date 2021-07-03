# Robot-operating-system-installation-and-configuration

In this project, we want to create a robot arm, and to start we need to create a simulation of the robot arm using a robot operating system AKA “ROS”.

ROS can be either be installed on Ubuntu using Virtual Box or it can be found online using https://www.theconstructsim.com/, I chose to work with the online tool as working with ubuntu requires a lot of the PC space. However, by using the online tool you will notice some difficulties as it doesn’t support all the existing functions as ubuntu.

## Start a new project
After signing up at https://www.theconstructsim.com/, click on create a project and the following screen will appear. start filling the blanks by writing the project name, choose which ROS version you want to work with, and in my case I’m working with ROS Melodic, and finally add a brief description then click create.

![image](https://user-images.githubusercontent.com/85634099/124360247-6622d880-dc31-11eb-95fa-09fd02b9d708.png)

## installing the package (arduino_robot_arm)
The next step is to clone the robot arm package from GitHub, so we will use the command (Sudo apt install git) to install Github on ROS to clone the project using its' path from GitHub to ROS.

![](https://user-images.githubusercontent.com/85634099/124360255-6de27d00-dc31-11eb-8177-fc9b4ffacb45.png)

## Install all the dependencies 
To run the package we need other dependencies (MoveIt, joint state publisher, gazebo ..etc), so we used the following commands to install those dependencies on ROS, and we complied the package after the installation is completed.

![](https://user-images.githubusercontent.com/85634099/124360261-7470f480-dc31-11eb-93d3-47d5581a7b30.png)
![](https://user-images.githubusercontent.com/85634099/124360266-78047b80-dc31-11eb-867e-a16a6b62b820.png)

## Controlling the motors
Now we run the robot arm package using the following command (roslaunch robot_arm_pkg check_motors.launch) which will result in two separate windows, where RVis window will show the arm structure simulation and the other is the joint state publisher window showing 4 controls to adjust the positioning of the parts.

![image](https://user-images.githubusercontent.com/85634099/124360282-894d8800-dc31-11eb-96b9-555cafa4f97e.png)

## Controlling the motors in simulation
using the following commands, now we will run the arm simulation on both RVis and Gazebo and adjust the arm using the controls.
$ roslaunch robot_arm_pkg check_motors.launch
$ roslaunch robot_arm_pkg check_motors_gazebo.launch

which will result in the following windows:

![](https://user-images.githubusercontent.com/85634099/124360294-9f5b4880-dc31-11eb-97fb-7e327c2df804.png)
![image](https://user-images.githubusercontent.com/85634099/124360313-bbf78080-dc31-11eb-9e9e-602111b73c55.png)
![image](https://user-images.githubusercontent.com/85634099/124360327-d4679b00-dc31-11eb-9329-3370c9119cff.png)

## MoveIt in RVis
To define the positioning of the arm and its' movements we use MoveIt which simulates the arm movement in different directions and scenarios (facing obstacles or not) and we can run it using the command (roslaunch moveit_pkg demo.launch) which will result in the following windows:

![image](https://user-images.githubusercontent.com/85634099/124360374-1a246380-dc32-11eb-91c3-1b190c9cfe68.png)
![image](https://user-images.githubusercontent.com/85634099/124360385-23153500-dc32-11eb-9483-970fa48d6d66.png)
![image](https://user-images.githubusercontent.com/85634099/124360386-27415280-dc32-11eb-836e-967a7b900b8f.png)



