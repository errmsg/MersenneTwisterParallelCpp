cmake_minimum_required(VERSION 2.8.9)
project(MersenneTwisterParallelCpp)
include_directories(include)
add_executable(serialTest "tests/catchTestSerial.cpp")
