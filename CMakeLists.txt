cmake_minimum_required(VERSION 3.8)
project(ur3e_interface_msgs)

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

# Specify the ROS messages
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/PersonInfo.msg"
  "msg/PeopleInfo.msg"
)

ament_export_dependencies(rosidl_default_runtime)

ament_package()
