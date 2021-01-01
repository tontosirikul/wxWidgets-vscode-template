cmake_minimum_required(VERSION 3.11.3)

set(CMAKE_CXX_STANDARD 17)

project(hello-world)

find_package(wxWidgets REQUIRED COMPONENTS core base)
include(${wxWidgets_USE_FILE})

file(GLOB project_SRCS src/*.cpp)

add_executable(hello-world ${project_SRCS})
target_link_libraries(hello-world ${wxWidgets_LIBRARIES})
target_include_directories(Hhello-world PRIVATE ${wxWidgets_INCLUDE_DIRS})
