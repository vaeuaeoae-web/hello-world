#大作业
cmake_minimum_required(VERSION 3.16)
project(MusicPlayer VERSION 1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_AUTOMOC ON)

find_package(Qt6 COMPONENTS Core Gui Widgets Multimedia MultimediaWidgets REQUIRED)

add_executable(${PROJECT_NAME} WIN32    
    main.cpp
    MainWindow.cpp
    Playlist.cpp
    Player.cpp
    LrcParser.cpp
    LyricsModel.cpp
    LyricsWidget.cpp
    Transcoder.cpp
    app.rc
)

target_link_libraries(${PROJECT_NAME} PRIVATE
    Qt6::Core
    Qt6::Gui
    Qt6::Widgets
    Qt6::Multimedia
    Qt6::MultimediaWidgets
)
