cmake_minimum_required(VERSION 3.0.2)
project(mappingadapter)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rosbag
  std_msgs
)

 add_library(${PROJECT_NAME}
   src/mapping_adapter.cpp
 )
target_include_directories(${PROJECT_NAME} PUBLIC
        ${catkin_LIBRARIES}
)
install(TARGETS ${PROJECT_NAME}
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib
        RUNTIME DESTINATION bin
        PUBLIC_HEADER DESTINATION include
        )
