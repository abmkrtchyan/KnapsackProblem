cmake_minimum_required(VERSION 3.00)
project(KnapsackProblem)

set(CMAKE_CXX_STANDARD 20)

find_package(GTest REQUIRED)

add_executable(KnapsackProblem main.cpp)

add_executable(Tests tests/tests.cpp)

target_link_libraries(Tests PRIVATE GTest::GTest GTest::Main pthread)

add_test(NAME UnboundedKnapsackTests COMMAND Tests)