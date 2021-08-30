cmake_minimum_required(VERSION 3.20)
project(thread_lib)

set(CMAKE_CXX_STANDARD 14)

find_package(Threads)


add_executable(thread_lib main.cpp threadpool.h locker.h http_conn.cpp http_conn.h)

target_link_libraries(thread_lib ${CMAKE_THREAD_LIBS_INIT})