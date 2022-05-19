cmake_minimum_required(VERSION 3.22)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(hw3)

add_executable(solver equation.cpp)

include_directories(../formatter_ex_lib ../solver_lib)

add_subdirectory(../formatter_ex_lib formatter_ex)
add_subdirectory(../solver_lib solver_lib)

target_link_libraries(solver formatter_ex solver_lib)