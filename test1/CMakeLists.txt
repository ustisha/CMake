cmake_minimum_required(VERSION 3.0)

# Set a variable for commands below
set(PROJECT_NAME test1)

# Define your project and language
project(${PROJECT_NAME} C CXX)

get_board_id(board_id mini atmega328)

#message(${ARDUINO_SDK_LIBRARIES_PATH})
#message(${PROJECT_SOURCE_DIR})

add_arduino_executable(${PROJECT_NAME} ${board_id} main.cpp)
upload_arduino_target(${PROJECT_NAME} "${board_id}" COM6)

find_arduino_library(OneWire_Lib OneWire ${board_id})
link_arduino_library(${PROJECT_NAME} OneWire_Lib ${board_id})

find_arduino_library(DallasTemperature_Lib DallasTemperature ${board_id})
link_arduino_library(${PROJECT_NAME} DallasTemperature_Lib ${board_id})
