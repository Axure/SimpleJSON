cmake_minimum_required(VERSION 2.6)

project(SimpleJSON)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(SimpleJSON SimpleJSON/json.h SimpleJSON/json.cpp SimpleJSON/jparser.h SimpleJSON/jparser.cpp)
set_property(TARGET SimpleJSON PROPERTY CXX_STANDARD 14)

add_executable(Test SimpleJSON/main.cpp)
set_property(TARGET Test PROPERTY CXX_STANDARD 14)
target_link_libraries(Test SimpleJSON)