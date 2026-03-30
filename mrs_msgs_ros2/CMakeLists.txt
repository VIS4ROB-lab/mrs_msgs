cmake_minimum_required(VERSION 3.5)
project(mrs_msgs)

# Ensure GLOB_RECURSE does not follow symlinks by default
cmake_policy(SET CMP0009 NEW)

set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(ament_cmake REQUIRED)
find_package(builtin_interfaces REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)
find_package(sensor_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)

# automatically discover all message and service files from subdirectories only
file(GLOB_RECURSE msg_files FOLLOW_SYMLINKS FALSE RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} 
  "msg/*.msg"
)

rosidl_generate_interfaces(${PROJECT_NAME}
    ${msg_files}
    DEPENDENCIES builtin_interfaces geometry_msgs std_msgs sensor_msgs
  )

ament_package()
