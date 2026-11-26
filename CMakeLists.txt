cmake_minimum_required(VERSION 3.15)
project(cg)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(MSVC)
  add_compile_options(/W4)
  set(CMAKE_C_FLAGS_DEBUG "/Zi /Od /fsanitize=address")
  set(CMAKE_CXX_FLAGS_DEBUG "/Zi /Od /fsanitize=address")
else()
  add_compile_options(-Wall -Wextra -pedantic)
  set(CMAKE_C_FLAGS_DEBUG "-g -ggdb3 -fsanitize=address -fno-omit-frame-pointer")
  set(CMAKE_CXX_FLAGS_DEBUG "-g -ggdb3 -fsanitize=address -fno-omit-frame-pointer")
endif()

add_subdirectory(vk)
