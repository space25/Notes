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
   mkdir ros_ws && cd ros_ws && mkdir src && colcon build
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
   pip --no-cache-dir install numpy empy lark
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
