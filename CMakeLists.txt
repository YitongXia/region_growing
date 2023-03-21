cmake_minimum_required(VERSION 3.22)
project(region_growing)

set(CMAKE_CXX_STANDARD 14)

add_executable(region_growing main.cpp)

find_package(CGAL REQUIRED)
include(${CGAL_USE_FILE})
target_link_libraries(region_growing ${CGAL_LIBRARIES})