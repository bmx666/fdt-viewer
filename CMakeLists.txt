cmake_minimum_required(VERSION 3.12)

project(fdt-viewer VERSION 0.8.1 LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt5 COMPONENTS Widgets REQUIRED)

add_subdirectory("src")

if (UNIX)
    install(FILES resources/fdt-viewer.svg DESTINATION share/icons/hicolor/scalable/apps)
    install(FILES resources/fdt-viewer.desktop DESTINATION share/applications)
endif (UNIX)
