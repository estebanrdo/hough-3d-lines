cmake_minimum_required(VERSION 3.5.0 FATAL_ERROR)

project(hough3dlines LANGUAGES CXX)

set(CMAKE_DEBUG_POSTFIX d)
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -D_DEBUG")

find_package(Eigen3 REQUIRED NO_MODULE)

add_executable(${PROJECT_NAME}
               hough3dlines.cpp
               hough.cpp
               hough.h
               pointcloud.cpp
               pointcloud.h
               sphere.cpp
               sphere.h               
               vector3d.cpp
               vector3d.h)
               
target_link_libraries (${PROJECT_NAME} Eigen3::Eigen)