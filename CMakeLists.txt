cmake_minimum_required(VERSION 3.13.0)

project(DirectXTex)  

file(GLOB_RECURSE SOURCE_FILES "DirectXTex/*.cpp" "DirectXTex/*.h" )

set(COMMON_CXX_FLAGS "${COMMON_CXX_FLAGS}  /std:c++17 /W4 /arch:AVX2 /fp:fast /MP")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${COMMON_CXX_FLAGS}")

message(STATUS "Generating project file for ${PROJECT_NAME} in ${PROJECT_SOURCE_DIR}")

add_library(${PROJECT_NAME} STATIC ${SOURCE_FILES})