cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

project(Project)
find_package(Qt5 COMPONENTS Widgets REQUIRED)

add_executable(main.out main.cpp window.cpp)

target_link_libraries(main.out Qt5::Widgets)
