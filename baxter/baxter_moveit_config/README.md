# Baxter MoveIt!
Author: Rethink Robotics Inc.

Website: https://github.com/RethinkRobotics/sdk-examples

MoveIt! configuration package for the Baxter Research Robot from Rethink Robotics.

## PACKAGE DEPENDENCIES
To use the baxter_moveit_config package you will need the baxter_description package containing Baxter's URDF. This package is available for download at the following repository:

   git clone https://github.com/RethinkRobotics/baxter_common.git

## Generate SRDF with XACRO

To use the setup assistant, generate the latest baxter.srdf from the xacro file:

    xacro `rospack find baxter_moveit_config`/config/baxter.srdf.xacro left_electric_gripper:=true right_electric_gripper:=true left_tip_name:=left_gripper right_tip_name:=right_gripper > config/baxter.srdf

## Note on warnings: 
When using `kinematics_solver: kdl_kinematics_plugin/KDLKinematicsPlugin` there will be a warning that the `Kinematics solver doesn't support #attempts anymore, but only a timeout. Please remove the parameter '/ns/group/left_arm/kinematics_solver_attempts' from your configuration.` This is a warning that was depreciated in PR #1288, Jan-2019. This warning has no impact on function. 

