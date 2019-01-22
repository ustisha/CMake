set(CMAKE_TOOLCHAIN_FILE ./arduino-cmake-ng/cmake/Arduino-Toolchain.cmake) # Arduino Toolchain

cmake_minimum_required(VERSION 3.0)
#====================================================================#
#  Setup Project                                                     #
#====================================================================#
project(CMake C CXX)

# add the project directory into build
add_subdirectory(test1)
