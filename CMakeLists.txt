cmake_minimum_required (VERSION 3.10)
project (PythonCpp)

set(CMAKE_CXX_FLAGS_DEBUG "-g")
set(CMAKE_CXX_FLAGS_RELEASE "-O3")
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(EXE main)

include_directories(
  /usr/include/python2.7
)

add_executable(${EXE} main.cpp)
target_link_libraries(
  ${EXE}
  /usr/lib64/libpython2.7.so
)