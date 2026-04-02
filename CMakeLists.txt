cmake_minimum_required (VERSION 3.10)
project ("bin2cpp")

set(CMAKE_CXX_STANDARD 23)

add_executable(${PROJECT_NAME} "Source/Main.cpp")

target_include_directories(${PROJECT_NAME}
PUBLIC 
    "Headers"
)

if (${CMAKE_BUILD_TYPE} MATCHES "Debug")
    add_definitions(-D_DEBUG)
endif()
