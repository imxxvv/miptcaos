cmake_minimum_required(VERSION 3.15)
project(CalcProject VERSION 1.2.3)

set(CMAKE_CXX_STANDARD 17)

configure_file(version.h.in version.h @ONLY)

add_executable(calculator main.cpp calc.cpp)

target_include_directories(calculator PRIVATE ${CMAKE_CURRENT_BINARY_DIR})

target_compile_definitions(calculator PRIVATE
    $<$<CONFIG:Debug>:DEBUG_MODE>
)
