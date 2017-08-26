
##############################################
#VARIABLES 
#${CMAKE_SOURCE_DIR}  : path of CMakeLists.txt
##############################################



# Specify the minimum version for CMake
cmake_minimum_required (VERSION 2.6)



# Project's name
project (Tutorial)


# The version number.
# 2 variables for minor and major versions
set (Tutorial_VERSION_MAJOR 1)
set (Tutorial_VERSION_MINOR 0)

# PASSING CONSTANTS FROM CMAKELISTS TO SOURCE CODE
# CMAKE AND SOURCE CODE INTERACTION
# configure a header file to pass some of the CMake settings
# to the source code
 configure_file (
  "${PROJECT_SOURCE_DIR}/TutorialConfig.h.in"
  "${PROJECT_BINARY_DIR}/TutorialConfig.h"
  )


# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
include_directories("${PROJECT_BINARY_DIR}")




#Code to build
add_executable(Tutorial tutorial.cpp)