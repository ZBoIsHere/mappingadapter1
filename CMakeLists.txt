cmake_minimum_required(VERSION 3.0.2)
project(mappingadapter)

find_package(catkin REQUIRED COMPONENTS
    roscpp
    rosbag
    std_msgs
)

find_package(PCL REQUIRED COMPONENTs
    common
    io
)

include_directories(
    ${catkin_INCLUDE_DIRS}
    ${PCL_INCLUDE_DIRS}
        ${PROJECT_SOURCE_DIR}/include
)

add_library(${PROJECT_NAME} SHARED
    src/mapping_adapter.cpp
 )


target_include_directories(${PROJECT_NAME} PUBLIC
    ${catkin_LIBRARIES}
    ${PCL_LIBRARIES}
    pcl_common
    pcl_io
)
