cmake_minimum_required(VERSION 3.24)

project(gherkin-cpp-container VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED On)

set_directory_properties(PROPERTY USE_FOLDERS ON)
include(FetchContent)

add_executable(gherkin-cpp-container main.cpp)

add_subdirectory(extern)

target_link_libraries(gherkin-cpp-container PRIVATE
    gherkin-cpp
)
