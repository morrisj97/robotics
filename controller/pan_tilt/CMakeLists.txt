cmake_minimum_required(VERSION 2.8.3)
project(pan_tilt)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  message_generation
)

################################################
## Declare ROS messages, services and actions ##
################################################

## Generate messages in the 'msg' folder
add_message_files(
   FILES
   PanTilt.msg
 )

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

###################################
## catkin specific configuration ##
###################################
catkin_package(
  CATKIN_DEPENDS rospy std_msgs message_runtime
)

###########
## Build ##
###########

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

