cmake_minimum_required(VERSION 3.0)
#====================================================================#
#  Setup Project                                                     #
#====================================================================#
project(CMake C CXX)

set(ARDUINO_CMAKE_SKETCHBOOK_PATH "${CMAKE_CURRENT_LIST_DIR}")

# add the project directory into build
add_subdirectory(test1)
