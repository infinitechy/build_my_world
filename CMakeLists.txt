cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project("example1")
find_package(gazebo REQUIRED)
include_directories(${GAZEBO_INCLUDE_DIRS})
link_directories(${GAZEBO_LIBRARY_DIRS})
list(APPEND CMAKE_CXX_FLAGS "${GAZEBO_CXX_FLAGS}")

add_library(example1 SHARED script/example1.cpp)
target_link_libraries(example1 ${GAZEBO_LIBRARIES})
