cmake_minimum_required(VERSION 3.19)
project(DataStructure)

set(CMAKE_CXX_STANDARD 14)

set(Sophus_DIR "/home/xiujie/SLAM_Lib/Sophus/build")


# 为使用 sophus，您需要使用find_package命令找到它
find_package( Sophus REQUIRED )


include_directories( ${Sophus_INCLUDE_DIRS} )
include_directories("/usr/include/eigen3")

add_executable(DataStructure main.cpp)
target_link_libraries( DataStructure  ${Sophus_LIBRARIES} )


