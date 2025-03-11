cmake_minimum_required(VERSION 3.26)
project(libhttp)

file(GLOB LIBHTTP_SRC ${PROJECT_SOURCE_DIR}/src/*.c)

add_library(libhttp SHARED ${LIBHTTP_SRC})
add_library(libhttp-static STATIC ${LIBHTTP_SRC})
target_include_directories(libhttp PUBLIC ${PROJECT_SOURCE_DIR}/include)
target_include_directories(libhttp-static PUBLIC ${PROJECT_SOURCE_DIR}/include)