# travelable_region  
An implementation of GP-INSAC algorithm  
Author: Huang Pengdi  
Email:alualu628628@163.com  
  
This is a implementation of GP-INSAC algorithm in ROS system  
The full name of GP-INSAC algorithm is Gaussian Process INSAC algorithm  
  
  
It is firstly proposed by B. Douillard et al. in the paper:   
Douillard B, Underwood J, Kuntz N, et al, On the segmentation of 3D LIDAR point clouds, IEEE ICRA 2011, 2798-2805.  

This algorithm is to obtain the travelable region (ground points) of a read-time point clouds (one frame online point cloud)  
**Note** that the input topic of GP-INASC is macthing with the output topic of [LOAM](https://github.com/laboshinl/loam_velodyne.git)

## Installation
Makesure you have a ubuntu14.04 system and a ROS system [ROS - Indigo](http://www.ros.org/), I think indigo or higher version is fine.    
cd $YOUR_WORKSPACE_DIR$, and type:
```
catkin_make -DCMAKE_BUILD_TYPE=Release
```

## Running
Most of the algorithm parameters are declared in GP-INASC/launch/gpinsac.launch, including input topic and output topic.    
Run this node after modifying $<param name="lidar_topic">$ to your real-time point cloud topic:    
```
roslaunch travelable_region gp_insac.launch 
```

If you still do not know how to deal with your configuration, here a example [Husky_Simulation](https://github.com/alualu628628/Husky_Simulation.git) may be helpful, in which this node is used for real-time ground extraction.  
