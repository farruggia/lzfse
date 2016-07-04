project(lzfse)
cmake_minimum_required(VERSION 2.8.7)

set(CMAKE_C_FLAGS "-O3 -march=native -Wall -Wno-unknown-pragmas -Wno-unused-variable -DNDEBUG -D_POSIX_C_SOURCE -std=c99 -fvisibility=hidden")

include_directories(include/lzfse)

file(GLOB libraries lib/*.c*)
add_library(${PROJECT_NAME} ${libraries})
