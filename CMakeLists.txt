cmake_minimum_required(VERSION 2.8)

set(PROJECT_NAME CmakeTest)
project(${PROJECT_NAME})

set(MyLib1 MyLib1)

set(CMAKE_CONFIGURATION_TYPES "Debug;Release" CACHE STRING "Configs" FORCE)
if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

file(GLOB hdrs "*.h*")
file(GLOB srcs "*.cpp")


add_executable(${PROJECT_NAME} ${srcs} ${hdrs})

add_subdirectory(lib1)
target_link_libraries(${PROJECT_NAME} ${MyLib1})