cmake_minimum_required(VERSION 3.12)
project(fluid-sim)
set(CMAKE_CXX_STANDARD 17)

add_subdirectory(lib/piksel)

set(SOURCES
    src/main.cpp
    src/app.cpp
)
add_executable(index ${SOURCES})
target_include_directories(index
    PUBLIC src
    PUBLIC lib/piksel/src
)
target_link_libraries(index
    piksel
)
