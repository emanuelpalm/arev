cmake_minimum_required(VERSION 3.12)
project(arev_http C)

set(
    SOURCE_FILES
    include/arev/http.h
    src/http.c
)
add_library(arev_http STATIC ${SOURCE_FILES})
target_include_directories(
    arev_http
    PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
)
