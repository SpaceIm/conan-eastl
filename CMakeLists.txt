cmake_minimum_required(VERSION 3.1.2)
project(cmake_wrapper)

if(EXISTS "${CMAKE_BINARY_DIR}/conanbuildinfo.cmake")
  include("${CMAKE_BINARY_DIR}/conanbuildinfo.cmake")
else()
  include(conanbuildinfo.cmake)
endif()
conan_basic_setup(TARGETS)

set(CMAKE_CXX_STANDARD 14)

add_subdirectory("source_subfolder")
