### Installation:
1. Install [ROS](https://ros.org/)
1. Install build tools:
   ```
   sudo apt install python3-colcon-common-extensions
   ```
1. Add to .bashrc file:
   ```
   source /opt/ros/<ros_version>/setup.bash
   source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash
   ```
1. Create warkspace:
   ```
   mkdir ros_workspace && cd ros_workspace && mkdir <ProjectName> && cd <ProjectName> && mkdir src && colcon build
   ```
1. Add lockal setup to .bashrc:
   ```
   source ~/ros_ws/install/setup.bash
   ```
1. Install tutorial:
   ```
   sudo apt install ros-humble-urdf-tutorial
   ```
1. Install python dependencies:
   ```
   pip3 --no-cache-dir install numpy empy lark
   ```
   ```
   sudo apt-get install ros-humble-imu-tools
   ```
1. Install Gazebo
   ```
   sudo apt install ros-humble-gazebo*
   or
   sudo apt install gazebo
   ```
1. [Optional] Fix python build
   ```
   pip3 list | grep setuptools
   ```
   need version 58.2.0
   ```
   pip3 --no-cache-dir install setuptools==58.2.0
   ```
   ```
   pip3 list | grep setuptools
   ```
### Development:
1. Create packages:
   ```
   ros2 pkg create <python_pkg_name> --build-type ament_python --dependencies rclpy
   or
   ros2 pkg create <cpp_pkg_name> --build-type ament_cmake --dependencies rclcpp
   ```
1. Build appication:
   ```
   colcon build
   or
   colcon build --packges-select <pkg_name>
   or
   colcon build --symlink-install
   ```
1. Run:
   ```
   ros2 run <package_name> <executable>
   ```
1. Check list of running nodes:
   ```
   ros2 node list
   ```
1. Check topics information type:
   ```
   ros2 topic list
   ```
1. Check service list:
   ```
   ros2 service list
   ```
1. Print topic information:
   ```
   ros2 topic echo /<topic_name>
   ros2 topic info /<topic_name>
   ros2 node info /<node_name>
   ros2 interface show example_interfaces/msg/String
   ros2 topic hz /<topic_name> # publishing frequency
   ros2 topic bw /<topic_name>

   ros2 service type /<service_name>
   
   ```
1. Rename a node in runtime:
   ```
   ros2 run <package_name> <executable> --ros-args --remap __node:=<new_name>
   ```
1. Show massages in packages:
   ```
   ros2 interface package sensor_msgs
   ```
1. Check number of parameres of a node:
   ```
   ros2 param list
   or
   ros2 param get /<node_name> <param_name>
   ```
1. Pipeline:
   ```
   ros2 node list
   ros2 node info /<node_name>
   ros2 topic list
   ros2 topic info /<topic_name>
   ros2 interface show <message_type>
   ```
1. Run Launch file
   ```
   ros2 launch <package_name> <name_of_launch_file>
   ```
### Tools
1. Gazebo
2. rqt_graph
   ```
   rqt_graph
   ```
