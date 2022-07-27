* 操作步骤
  * 在工程目录下创建目录thirdparty
  * 在根目录下的CMakeLists.txt文件中添加
    * add_subdirectory(thirdparty/mappingadapter)
    * include_directories(${PROJECT_SOURCE_DIR}/thirdparty/mappingadapter/include)
    * target_link_libraries(${YOUR_PROJECT_NAME} mappingadapter)
  * 根据您的项目，选择合适的类继承mappingadapter，并实现两个纯虚函数，具体可以参考https://github.com/ZBoIsHere/r3live
