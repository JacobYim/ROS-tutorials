cmake_minimum_required(VERSION 3.0.2)
project(ros_tutorials)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
)
catkin_package(CATKIN_DEPENDS roscpp std_msgs)
include_directories(${catkin_INCLUDE_DIRS})
add_executable(hello_world_node src/hello_world_node.cpp)
target_link_libraries(hello_world_node ${catkin_LIBRARIES})
