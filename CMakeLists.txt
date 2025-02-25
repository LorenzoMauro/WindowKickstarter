cmake_minimum_required(VERSION 3.15)
project(WindowKickStarter CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_TOOLCHAIN_FILE "${CMAKE_SOURCE_DIR}/external/vcpkg/scripts/buildsystems/vcpkg.cmake")

find_package(glfw3 CONFIG REQUIRED)
find_package(OpenGL REQUIRED)

add_subdirectory(src)

