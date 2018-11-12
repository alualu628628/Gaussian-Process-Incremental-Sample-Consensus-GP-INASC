# travelable_region
An implementation of GP-INSAC algorithm
Author: Huang Pengdi
Email:alualu628628@163.com
This is a implementation of GP-INSAC algorithm in ROS system
The full name of GP-INSAC algorithm is Gaussian Process INSAC algorithm
It is firstly proposed by B. Douillard et al. in the paper:
Douillard B, Underwood J, Kuntz N, et al, On the segmentation of 3D LIDAR point clouds, IEEE ICRA 2011, 2798-2805.

This algorithm is to obtain the travelable region (ground points) of a given point cloud scene by a real time processing way
The input is output topic of the LOAM algorithm, which is at 
https://github.com/laboshinl/loam_velodyne.git

how to compile it?
catkin_make is enough

how to use it?
roslaunch travelable_region gp_insac.launch 
