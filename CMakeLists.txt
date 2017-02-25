cmake_minimum_required(VERSION 2.6)

project(SimpleJSON)

add_library(SimpleJSON SimpleJSON/json.h SimpleJSON/json.cpp SimpleJSON/jparser.h SimpleJSON/jparser.cpp)

add_executable(Test SimpleJSON/main.cpp)
target_link_libraries(Test SimpleJSON)