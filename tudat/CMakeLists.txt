cmake_minimum_required(VERSION 3.28.1)

# Metadata
project("tudat")

# Compilation
set (CMAKE_CXX_STANDARD 20)

# Build configuration
set (CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set (CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/lib)
set (CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/lib)

# Install configuration
set (INSTALL_LIB_DIR ${CMAKE_INSTALL_PREFIX}/lib)
set (INSTALL_BIN_DIR ${CMAKE_INSTALL_PREFIX}/bin)
set (INSTALL_INCLUDE_DIR ${CMAKE_INSTALL_PREFIX}/include)

# Resources
include_directories(${CMAKE_SOURCE_DIR}/include)

# Build library
add_library(tudat STATIC src/types.cpp)

# Install
install (DIRECTORY lib/ DESTINATION ${INSTALL_LIB_DIR})
install (DIRECTORY include/ DESTINATION ${INSTALL_INCLUDE_DIR}/tudat)
