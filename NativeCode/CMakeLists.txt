
##############################################
#VARIABLES 
#${CMAKE_SOURCE_DIR}  : path of CMakeLists.txt
##############################################



# Specify the minimum version for CMake
cmake_minimum_required(VERSION 2.8)



# Project's name
project(hello)


#SET VARIABLES
#CMAKE_BINARY_DIR = bin
#EXECUTABLE_OUTPUT_PATH = ./bin
#LIBRARY_OUTPUT_PATH = ./bin

# Set the output folder where your program will be created
set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR})

# The following folder will be included
include_directories("${PROJECT_SOURCE_DIR}")