cmake_minimum_required(VERSION 3.0.0)

project(Calculator_Project VERSION 1.0.0)


add_subdirectory(my_math)

add_subdirectory(my_print)


add_executable(calculator
main.cpp)


target_link_libraries(calculator PRIVATE my_math  my_print)

message("CMAKE_INSTALL_PREFIX = ${CMAKE_INSTALL_PREFIX}")
message("CMAKE_SOURCE_DIR = ${CMAKE_SOURCE_DIR}")
message("CMAKE_CURRENT_SOURCE_DIR = ${CMAKE_CURRENT_SOURCE_DIR}")
message("CMAKE_MODULE_PATH = ${CMAKE_MODULE_PATH}")

#other modifications are in subdirectory level CMakeLists.txt
#check the file at my_math/CMakeLists.txt




