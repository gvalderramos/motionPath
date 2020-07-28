cmake_minimum_required(VERSION 2.6)
project(tcMotionPath)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/modules)
add_subdirectory(source)