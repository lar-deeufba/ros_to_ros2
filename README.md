# ros_to_ros2
Repository dedicated to ease the way from ROS1 to ROS2 by providing a cheatsheet and examples to be ran.

## Useful Commands

- To find where a package is located:
Before: `$ rospack find $PACKAGE_NAME`
Now: `$ ros2 pkg prefix $PACKAGE_NAME`

- Accessing a package’s path:
Before: `$ roscd PACKAGE_NAME`
Now: `$ colcon_cd PACKAGE_NAME`

- Creating a package. It differs for a Python and CPP package. We still have `CMakeList` and `package.xml` manifest. In Python we don’t need a CMakeList, but a [setup.py](http://setup.py) and then colcon build to build it.
Before: `$ catkin_create_package PACKAGENAME`
Now: `$ ros2 pkg create PACKAGE_NAME —build-type ament`

- Displaying a message:
Before: `$ rosmsg show geometry_msgs/Twist`
Now: `$ ros2 interface show std_msgs/msg/String`

- Output tf tree to a pdf:
Now: `$ ros2 run tf2_tools view_frames.py`

- Monitoring the tf tree
Now: `$ ros2 run tf2_ros tf2_monitor`
