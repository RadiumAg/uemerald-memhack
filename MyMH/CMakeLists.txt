cmake_minimum_required(VERSION 3.1.0)

project(MyMH VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

if(CMAKE_VERSION VERSION_LESS "3.7.0")
    set(CMAKE_INCLUDE_CURRENT_DIR ON Gui)
endif()

find_package(Qt5 COMPONENTS Widgets REQUIRED)

add_executable(MyMH
    widget.ui
    widget.cpp
    main.cpp
    img.qrc
)

target_link_libraries( Qt5::Widgets)
