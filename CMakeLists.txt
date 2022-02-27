# Generated from rasterwindow.pro.

cmake_minimum_required(VERSION 3.16)
project(cpp_empty_project LANGUAGES CXX)
set(VENDOR_DIR ${CMAKE_SOURCE_DIR}/vendor)

add_subdirectory(${VENDOR_DIR}/LuaBridge)
add_subdirectory(${VENDOR_DIR}/lua)


add_subdirectory(myproject)
