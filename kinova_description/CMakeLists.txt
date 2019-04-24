cmake_minimum_required(VERSION 2.8.3)
project(kinova_description)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}  -std=c++0x")

find_package(catkin REQUIRED COMPONENTS
  urdf
  xacro)

catkin_package()

install(DIRECTORY launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY meshes
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
   FILES_MATCHING PATTERN "*.dae"
 )
#install(DIRECTORY config DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
