cmake_minimum_required(VERSION 3.10)
project(tinyeditor CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Curses REQUIRED)

include_directories(${CURSES_INCLUDE_DIR})

add_executable(tinyeditor
    src/main.cpp
)
target_link_libraries(tinyeditor ${CURSES_LIBRARIES})