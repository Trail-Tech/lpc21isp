cmake_minimum_required(VERSION 3.4)
enable_language("C")
enable_language("CXX")
find_package (Threads)

# ProjDirPath is the directory that holds main.c
SET(ProjDirPath ${CMAKE_CURRENT_SOURCE_DIR})

include_directories(
    .)


Project(lpc21isp)

#add_compile_options( -wall )

set(CMAKE_COLOR_MAKEFILE ON)

set(SOURCE
    adprog.c
    lpcprog.c
    lpcterm.c
    lpc21isp.c
    )

add_executable (lpc21isp ${SOURCE})

INSTALL(TARGETS lpc21isp DESTINATION bin)
