# lms5xx
Driver for the Sick lms5xx in ROS Jade (might work for other versions).

With this driver already contains a version of sicktoolbox(2) so need for it.
This driver will create a LaserScan topic under the name /Scan that you can subscripe to.

Install:
1. Create a catkin package with the name laser_node.
2. Delete all the files in the package.
3. Copy the contents of the file in the catking package.
4. Go to lms5xx_node.cpp in src and alter the ip adress to the one of you're Sick lms5xx.
4. Go to the source of the catkin_workspace and use catkin_make.
5. Use the command "devel/setup.bash"

Test:
  The node is started by invoking "rosrun laser_node laser_node". 
  The resulted scan can be tested by "rostopic echo /Scan". (should you not be able to find it use "rostopic list" to find the alternative name)
  
DISCLAIMER:
  I am not the creator of the drivers or node. I merely rebuild the package from scratch and altered the source files to make it work in 
  ROS jade.
