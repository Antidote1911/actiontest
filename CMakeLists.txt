cmake_minimum_required(VERSION 3.19)
project(sans_titre LANGUAGES CXX)

find_package(Qt6 6.8.2 REQUIRED COMPONENTS Core Widgets)
set(CMAKE_CXX_STANDARD 20)

qt_standard_project_setup()

qt_add_executable(sans_titre
    WIN32 MACOSX_BUNDLE
    main.cpp
    mainwindow.cpp
    mainwindow.h
    mainwindow.ui
)

target_link_libraries(sans_titre
    PRIVATE
        Qt::Core
        Qt::Widgets
)

include(GNUInstallDirs)

