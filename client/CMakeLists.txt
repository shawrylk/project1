cmake_minimum_required(VERSION 2.8.4)

project(client)

#find_package(OpenCV REQUIRED)

#link_libraries(${OpenCV_LIBS})

#include_directories(${OpenCV_INCLUDE_DIRS})
include_directories(include)

#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "src/*.c")

set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR})

add_executable(${PROJECT_NAME} ${SOURCES})

#target_link_libraries(client ${OpenCV_LIBS})
target_link_libraries(${PROJECT_NAME})
