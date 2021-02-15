# ** "Simulation of open manipulator and realsense2_d435 camera using Gazebo & RoS" **

----------

## 1. Clone and build Realsense-ros-gazebo 
   Please refer to https://github.com/rickstaa/realsense-ros-gazebo

## 2. Modify urdf file: cjs_robot_description/urdf/open_manipulator.urdf.xacro
   Add the following contents
   
    <xacro:include filename="$(find realsense2_description)/urdf/_d435.urdf.xacro" />  
    <xacro:sensor_d435 parent="link5" use_nominal_extrinsics="true">
      <origin xyz="0 0 0.05" rpy="0 0 0"/>
    </xacro:sensor_d435>
  

## 3. Execute following commands in the individual command shell.

   2.1. `$ roslaunch cjs_robot_gazebo bringup.launch`

   2.2. `$ roslaunch cjs_robot_moveit_config move_group.launch`

   2.3. `$ roslaunch cjs_robot_moveit_config moveit_rviz.launch rviz_config:='rospack find cjs_robot_moveit_config\'/launch/moveit.rviz`

