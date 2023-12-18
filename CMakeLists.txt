cmake_minimum_required(VERSION 3.27)
project(k_gnn)

set(CMAKE_CXX_STANDARD 14)

#enable_language(CUDA)
include_directories(
        cpu
        "C:\\Users\\aaron\\windows-venv\\Lib\\site-packages\\torch\\include"
        "C:\\Users\\aaron\\windows-venv\\Lib\\site-packages\\torch\\include\\torch\\csrc\\api\\include"
)
#include_directories(SYSTEM "C:\\Users\\aaron\\windows-venv\\Lib\\site-packages")
#include_directories("C:\\Users\\aaron\\windows-venv\\Lib\\site-packages\\torch\\share\\cmake")

#find_package(CUDA REQUIRED)
#find_package(Torch REQUIRED)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${TORCH_CXX_FLAGS}")

add_executable(k_gnn
        cpu/adjacency.h
        cpu/assignment.h
        cpu/connect.h
        cpu/graph.cpp
        cpu/isomorphism.h
        cpu/iterate.h
        cpu/utils.h)

#target_link_libraries(k-gnn "${TORCH_LIBRARIES}")