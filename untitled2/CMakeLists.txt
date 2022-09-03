cmake_minimum_required(VERSION 3.23)
project(untitled2)

set(CMAKE_CXX_STANDARD 14)

add_executable(untitled2 main.cpp)

add_subdirectory(module1)
add_subdirectory(module2)

target_include_directories(untitled2 PRIVATE module1 module2)


target_link_libraries(untitled2 PRIVATE module1_t module2_t)