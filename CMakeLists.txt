cmake_minimum_required(VERSION 3.17)
project(imgui)
set(CMAKE_CXX_STANDARD 17)

set(IMGUI_FILES
        imconfig.h
        imgui.cpp
        imgui.h
        imgui_demo.cpp
        imgui_draw.cpp
        imgui_internal.h
        imgui_tables.cpp
        imgui_widgets.cpp
        imstb_rectpack.h
        imstb_textedit.h
        imstb_truetype.h
        )


add_library(${PROJECT_NAME} STATIC
        ${IMGUI_FILES}
        )

target_include_directories(${PROJECT_NAME} PUBLIC
        .
        backends
        )
