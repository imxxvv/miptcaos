cmake_minimum_required(VERSION 3.15)
project(AutoDeps)

file(GLOB SOURCES "*.cpp")
add_executable(main ${SOURCES})
