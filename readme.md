# A ros gazebo plugin for pedestrians

This is a ros pkg for gazebo [actor](http://gazebosim.org/tutorials?tut=actor&cat=build_robot) plugin.

### Dependencies
* Ubuntu 18.04
* ROS-melodic
* Gazebo 9
* python-lxml
* turtlebot3
* turtlebot3_msgs
* turtlebot3_simulations

### Build

1. Add the repositories of [Gazebo 9](http://gazebosim.org/tutorials?tut=install_ubuntu) and [ROS kinetic](http://wiki.ros.org/indigo/Installation/Ubuntu)    

2. Install Gazebo 9, Ros melodic in buntu 18.04 and other dependencies.
```
sudo apt-get install ros-melodic-desktop-full
sudo apt-get install ros-melodic-gazebo9-ros-pkgs
```

3. Build packages

![rviz](./rviz_view.png)
![gazebo](./gazebo_view.png)

### Example
```
roslaunch turtlebot3_social default.launch
```

### Node Details
- **actor_plugin**    
  Build based on a [Gazebo official example](http://gazebosim.org/tutorials?cat=guided_i&tut=guided_i6). This node broadcasts the tf of every actor. [Social force model](http://vision.cse.psu.edu/courses/Tracking/vlpr12/HelbingSocialForceModel95.pdf) is applied in every actor to interactive with each other.

- **actor_services**    
  The python files help to create several gazebo sdf files quickly. There is a rviz file for visualization.

- **turtlebo3_social**    
  In our socially compliant pedestrian simulator, we collect data by mounting a depth sensor onto one of the pedestrians, to the height matching that of real-world setups. Then, the social force model, as described in the paper, is used to label each incoming depth
image with their corresponding social force.

- **data_collection**    
  To save the related dataset.


