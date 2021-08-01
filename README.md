# install-robot-arm-pakage-in-ROS

Robot arm package installation steps
====================================
After installing the ROS in Ubuntu follow these steps to install the arm package:
1. Create a workspase with Catkin  ``` mkdir -p ~/catkin_ra/src ```
2. Go to the workspase ``` cd ~/catkin_ra ```
3. Install the package in the workspase 
```
 catkin_make
cd ~/catkin_ra/src
git clone https://github.com/smart-methods/arduino_robot_arm.git
```
4. After clone the packge go back to catkin_ra ``` cd .. ```
5. Install the follwing commands
```
rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-kinetic-moveit

sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control
```
6. Go to bashrc folder 
```
sudo nano ~/.bashrc

# at the end of the (bashrc) file add the follwing line
source /home/ruba/catkin_ra/devel/setup.bash # write your own path 
then 
ctrl + o then ctrl+ x

source ~/.bashrc
```
7. Launch the package ``` roslaunch robot_arm_pkg check_motors.launch ```
