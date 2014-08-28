cmake_minimum_required (VERSION 2.6)
project(DenseTrajectories)

find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(Video Video.cpp)
target_link_libraries(Video ${OpenCV_LIBS}) 

add_executable(DenseTrack DenseTrack.cpp)
target_link_libraries(DenseTrack ${OpenCV_LIBS})
