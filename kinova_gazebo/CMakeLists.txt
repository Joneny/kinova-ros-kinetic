cmake_minimum_required(VERSION 2.8.3)
project(kinova_gazebo)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}  -std=c++0x")

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

install(DIRECTORY worlds
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
