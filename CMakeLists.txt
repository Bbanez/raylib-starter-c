cmake_minimum_required(VERSION 3.1)
project(raylib_starter VERSION 0.1.0)
add_executable(raylib_starter src/main.cpp)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

include_directories(${CMAKE_SOURCE_DIR}/external/raylib-5.5/src)

add_subdirectory(external/raylib-5.5)

target_include_directories(raylib_starter PUBLIC external/raylib-5.5/src)
target_link_libraries(raylib_starter PUBLIC raylib)
