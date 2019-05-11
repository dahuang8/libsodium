cmake_minimum_required(VERSION 2.8)
project(libsodium)
include(ExternalProject)
ExternalProject_Add(${PROJECT_NAME}
    BUILD_IN_SOURCE 1
    PREFIX ${CMAKE_SOURCE_DIR}
    INSTALL_DIR ${CMAKE_SOURCE_DIR}/Install
    DOWNLOAD_COMMAND ""
    WORKING_DIRECTORY ${CMAKE_SOURCE_DIR}
    SOURCE_DIR ${CMAKE_SOURCE_DIR}
    CONFIGURE_COMMAND ./autogen.sh COMMAND ./configure
    BUILD_COMMAND ${MAKE})

