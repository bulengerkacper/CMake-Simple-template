cmake_minimum_required(VERSION 3.19.0)
set(CMAKE_CXX_STANDARD 17)
project(ProjectName VERSION 0.1.0)

#implementation
file(GLOB_RECURSE sources CONFIGURE_DEPENDS "${CMAKE_CURRENT_SOURCE_DIR}/implementations/*.cpp")
add_executable(${PROJECT_NAME} ${sources} main.cpp)

####headers
target_include_directories(${PROJECT_NAME} PUBLIC PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>/headers)
