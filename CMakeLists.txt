
cmake_minimum_required(VERSION 3.17 FATAL_ERROR)

# Default to Debug
if(NOT CMAKE_BUILD_TYPE)
    message("Build type not specified, using Debug")
    set(CMAKE_BUILD_TYPE "Debug" CACHE STRING "Build type not specified, using Debug" FORCE)
endif(NOT CMAKE_BUILD_TYPE)

project(byacc LANGUAGES C)

include_directories(.)

add_executable(byacc
  closure.c
  error.c
  graph.c
  lalr.c
  lr0.c
  main.c
  mkpar.c
  mstring.c
  output.c
  reader.c
  yaccpar.c
  symtab.c
  verbose.c
  warshall.c)
