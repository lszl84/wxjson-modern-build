cmake_minimum_required(VERSION 3.17 FATAL_ERROR)

project(wxjson LANGUAGES CXX)

find_package(wxWidgets REQUIRED COMPONENTS net base core)

set(SRCS jsonreader.cpp jsonval.cpp jsonwriter.cpp)
add_library(wxjson ${SRCS})

include(${wxWidgets_USE_FILE})
target_link_libraries(wxjson PRIVATE ${wxWidgets_LIBRARIES})

message(STATUS "Project will be installed to ${CMAKE_INSTALL_PREFIX}")

install(TARGETS wxjson DESTINATION lib)
install(
    FILES json_defs.h jsonreader.h jsonval.h jsonwriter.h
    DESTINATION include/wxjson)