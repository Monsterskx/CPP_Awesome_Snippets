cmake_minimum_required(VERSION 2.8.12)
project(CPP_Ultimate_Snippets)
add_definitions("-fPIC -lgtest -lpthread")

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
file(GLOB_RECURSE SRC ${PROJECT_SOURCE_DIR}src/*)
add_executable(exec src/main.cpp ${SRC})
include_directories(${CMAKE_INCLUDE_PATH})

