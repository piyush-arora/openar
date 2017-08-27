
##############################################
#VARIABLES 
#${CMAKE_SOURCE_DIR}  : path of CMakeLists.txt
##############################################



# Specify the minimum version for CMake
cmake_minimum_required (VERSION 2.6)



# Project's name
project (Tutorial)


#build in only release mode
set(CMAKE_BUILD_TYPE Release)

#include directories
include_directories(include)


#Can manually add the sources using the set command as follows:
set(SOURCES src/Student.cpp)
 

#name of the executable and souce code to compile
add_library(testStudent STATIC ${SOURCES})


#Set the location for library installation -- i.e., /usr/lib in this case
# not really necessary in this example. Use "sudo make install" to apply
install(TARGETS testStudent DESTINATION /usr/lib)