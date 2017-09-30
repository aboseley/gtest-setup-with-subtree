cmake_minimum_required(VERSION 2.8.12)

project(Example)
include(CTest)

add_subdirectory( libs/googletest )

add_executable(example example.cpp)
target_link_libraries(example gtest gmock_main)

add_test(NAME example_test COMMAND example)
