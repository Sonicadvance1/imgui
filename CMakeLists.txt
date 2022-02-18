cmake_minimum_required(VERSION 3.0.0)
project(cmake_demo VERSION 0.1.0)

include(CTest)
enable_testing()

find_package(SDL2 REQUIRED)
add_executable(example_sdl_opengl3
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp
    backends/imgui_impl_sdl.cpp
    backends/imgui_impl_opengl3.cpp
    examples/example_sdl_opengl3/main.cpp)

include_directories(${CMAKE_SOURCE_DIR}
${CMAKE_SOURCE_DIR}/backends)
target_link_libraries(example_sdl_opengl3 PRIVATE SDL2::SDL2 GL)
set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
