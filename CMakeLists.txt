cmake_minimum_required(VERSION 3.7)
project(HelloSDL)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES main.cpp)
add_executable(HelloSDL ${SOURCE_FILES})

find_package(SDL2 REQUIRED)

include_directories(
        ${SDL2_INCLUDE_DIRS}
)

INCLUDE_DIRECTORIES(${PROJECT_NAME} ${SDL2_INCLUDE_DIRS})
set(SDL2_LIBRARIES "-L${SDL2_LIBDIR}  -lSDL2")
TARGET_LINK_LIBRARIES(${PROJECT_NAME} ${SDL2_LIBRARIES})
