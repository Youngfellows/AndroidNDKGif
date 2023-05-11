cmake_minimum_required(VERSION 3.4.1)

set(CMAKE_VERBOSE_MAKEFILE on)


set(SOURCES)
file(GLOB_RECURSE SOURCES "*.cpp")

add_library(androidndkgif SHARED ${SOURCES})

set(LIBS)
list(APPEND LIBS
        jnigraphics
        #android
        #GLESv2
        log
        )

target_link_libraries(androidndkgif ${LIBS})
