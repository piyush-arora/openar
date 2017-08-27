cmake_minimum_required(VERSION 2.8.9)
project (TestLibrary)

#For the shared library:
#set ( PROJECT_LINK_LIBS libtestStudent.so )
#link_directories( ~/exploringBB/extras/cmake/studentlib_shared/build )

#For the static library:
set ( PROJECT_LINK_LIBS libtestStudent.a )
link_directories(build )

include_directories(include)

add_executable(libtest tutorial.cpp)
target_link_libraries(libtest ${PROJECT_LINK_LIBS} )