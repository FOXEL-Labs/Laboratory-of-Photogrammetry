cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(stlplus C CXX)

FILE(GLOB LIBSLTPLUS_HPP_FILESYSTEM "${CMAKE_CURRENT_SOURCE_DIR}/filesystemSimplified/*.hpp" )
FILE(GLOB LIBSLTPLUS_CPP_FILESYSTEM "${CMAKE_CURRENT_SOURCE_DIR}/filesystemSimplified/*.cpp" )


LIST(APPEND LIBSLTPLUS_SRCS
  ${LIBSLTPLUS_HPP_FILESYSTEM} ${LIBSLTPLUS_CPP_FILESYSTEM})

INCLUDE_DIRECTORIES(./filesystemSimplified)
ADD_LIBRARY(stlplus ${LIBSLTPLUS_SRCS})
SET_PROPERTY(TARGET stlplus PROPERTY FOLDER OpenMVG/3rdParty)
