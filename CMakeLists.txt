# CMakeLists.txt
cmake_minimum_required(VERSION 3.28)

# set(CMAKE_C_COMPILER "C:/Program Files/LLVM/bin/gcc.exe")
# set(CMAKE_CXX_COMPILER "C:/Program Files/LLVM/bin/g++.exe")


project(HelloWorldProject)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(${PROJECT_NAME} main.cpp)

