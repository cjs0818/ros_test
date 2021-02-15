1. Clone and build Realsense-ros-gazebo (https://github.com/rickstaa/realsense-ros-gazebo)

2. Execute following commands in the individual command shell.

   2.1. $ roslaunch cjs_robot_gazebo bringup.launch

   2.2. $ roslaunch cjs_robot_moveit_config move_group.launch

   2.3. $ roslaunch cjs_robot_moveit_config moveit_rviz.launch rviz_config:=\`rospack find cjs_robot_moveit_config\`/launch/moveit.rviz

