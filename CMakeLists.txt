cmake_minimum_required(VERSION 3.20)
project(untitled11)

set(CMAKE_CXX_STANDARD 17)

set(PROJECT_HEADERS
        spaceObjects.h
        spaceShip.h
        parametrizationScreen.h
        camera.h
        functions.h
        )
set(PROJECT_SOURCES
        main.cpp
        spaceObjects.cpp
        spaceShip.cpp
        parametrizationScreen.cpp
        camera.cpp
        functions.cpp
        )
set(PROJECT_IMAGE
        space-shuttle.png
        spaceShip.png
        )
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR})

add_executable(untitled11 ${PROJECT_SOURCES} ${PROJECT_HEADERS})

set(SFML_STATIC_LIBRARIES TRUE)
set(SFML_DIR D:/SFML/lib/cmake/SFML)
find_package(SFML COMPONENTS system window graphics audio network REQUIRED)

include_directories(D:/SFML/include)
target_link_libraries(untitled11 sfml-system sfml-window sfml-graphics sfml-audio)
