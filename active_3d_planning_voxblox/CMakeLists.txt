cmake_minimum_required(VERSION 2.8.3)
project(active_3d_planning_voxblox)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

#add_definitions(-std=c++11)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


catkin_package()

cs_add_library(${PROJECT_NAME}
        src/map/voxblox.cpp
        src/initialization/voxblox_package.cpp
        )

cs_install()
cs_export()
