cmake_minimum_required(VERSION 2.6)

project(SimpleJSON)

add_library(SimpleJSON SimpleJSON/json.h SimpleJSON/json.cpp SimpleJSON/jparser.h SimpleJSON/jparser.cpp)
set_property(TARGET SimpleJSON PROPERTY CXX_STANDARD 11)

add_executable(Test SimpleJSON/main.cpp)
set_property(TARGET Test PROPERTY CXX_STANDARD 11)
target_link_libraries(Test SimpleJSON)