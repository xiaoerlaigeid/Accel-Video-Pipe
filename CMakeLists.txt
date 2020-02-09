cmake_minimum_required(VERSION 3.0)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)
project( video-analysis )
find_package( OpenCV REQUIRED )
find_package( Torch REQUIRED)
include_directories( ${OpenCV_INCLUDE_DIRS} )
add_executable( video-analysis video-analysis.cpp )
target_link_libraries( video-analysis ${OpenCV_LIBS} )
target_link_libraries( video-analysis "${TORCH_LIBRARIES}")