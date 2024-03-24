cmake_minimum_required(VERSION 3.5.0)

project(proxydroid
        VERSION 3.0.2
        LANGUAGES C CXX)

add_subdirectory(exec)
add_subdirectory(libevent)
add_subdirectory(redsocks)
