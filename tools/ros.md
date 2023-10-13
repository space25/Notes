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
1. Rename a node in runtime:
   ```
   ros2 run <package_name> <executable> --ros-args --remap __node:=<new_name>
   ```
