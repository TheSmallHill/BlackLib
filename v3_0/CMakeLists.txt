cmake_minimum_required (VERSION 2.8.3)
project (BlackLib)

if(UNIX)
    SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -std=gnu++0x")
endif()

# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
include_directories("${PROJECT_BINARY_DIR}")

# add the executable

add_library(BlackLib BlackCore.cpp BlackGPIO/BlackGPIO.cpp)
#target_link_libraries(BlackLib)
