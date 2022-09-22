cmake_minimum_required(VERSION 3.23)

project(Qt_OpenVPN CXX)

file(GLOB_RECURSE PROJECT_SOURCES CONFIGURE_DEPENDS src/*.c src/*.cpp src/*.hpp src/*.h)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 COMPONENTS
    Core
    Gui
    Widgets
REQUIRED)

add_executable(${PROJECT_NAME} ${PROJECT_SOURCES})
target_link_libraries(${PROJECT_NAME}
    Qt::Core
    Qt::Gui
    Qt::Widgets
)
