cmake_minimum_required (VERSION 2.8.11)
message("Building Driver for Linear Road")

project(DataDriver)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pthread")

add_library(LRDataProvider LRDataProvider.cpp MemTuples.cpp Tuple.cpp)

target_include_directories (LRDataProvider PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
