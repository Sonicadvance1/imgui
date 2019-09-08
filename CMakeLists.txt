set(NAME imgui)
set(SRCS imgui.cpp
  imgui_draw.cpp
  imgui_widgets.cpp
  addons/imguinodegrapheditor/imguinodegrapheditor.cpp
  addons/imguifilesystem/imguifilesystem.cpp)
add_library(${NAME} ${SRCS})
