cmake_minimum_required(VERSION 3.9)

project(hello_cmake.out)

set(EXECUTABLE_OUTPUT_PATH "..")

add_executable(hello_cmake.out
    hello_cmake.c)

# OpemMP stuff
find_package(OpenMP REQUIRED)
if(OpenMP_CXX_FOUND)
    target_link_libraries(hello_cmake.out PUBLIC OpenMP::OpenMP_CXX)
endif()
