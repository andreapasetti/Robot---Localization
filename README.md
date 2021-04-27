# Localization

With the adaptive monte carlo localization the robot can localize in the environment. A first guess of particles representing possible robot positions is generated. These particles will appear to be quite scattered. When the robot starts to move the particles will converge to the robot position. The project uses amcl package of ROS. The robot model is equipped with hokuyo lidar as rangefinder. Rviz is used to get the lidar measurements. Additionally the robot can be moved using teleop twist keyboard and particle convergence can be seen.

## Installation
- Initialize catkin workspace
- Clone the repository in your catkin "src" folder 

### Open terminal 1
```
catkin_make
source devel/setup.bash
roslaunch my_robot world.launch
```
### Open terminal 2
```
soruce devel/setup.bash
roslaunch my_robot/amcl.launch
```
Use "2D Nav Goal" to give a target position to the robot in Rviz

### Open terminal 3 (If you want to move the robot with the keyboard instead of "2D Nav Goal")
```
source devel/setup.bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
