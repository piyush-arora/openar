cmake_minimum_required(VERSION 2.8.9)
project (TestLibrary)

include_directories(include)
set ( PROJECT_LINK_LIBS libtestStudent.a )

set(SOURCES src/tutorial.cpp)

add_executable(libtest ${SOURCES})
target_link_libraries(libtest ${PROJECT_LINK_LIBS} )