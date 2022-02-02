cmake_minimum_required(VERSION 3.18)

project(AmazingSnakes)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory("${CMAKE_CURRENT_LIST_DIR}/glfw-3.3.6")

find_package(OpenGL REQUIRED)

add_executable(maze src/main.cpp)
target_link_libraries(maze glfw OpenGL::GL)