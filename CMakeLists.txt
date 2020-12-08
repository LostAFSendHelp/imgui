add_library(
    lafez-imgui

    lafez-imgui/imconfig.h
    lafez-imgui/imgui_draw.cpp
    lafez-imgui/imgui_internal.h
    lafez-imgui/imgui_widgets.cpp
    lafez-imgui/imgui.h
    lafez-imgui/imgui.cpp
    lafez-imgui/imstb_rectpack.h
    lafez-imgui/imstb_textedit.h
    lafez-imgui/imstb_truetype.h

    lafez-imgui/impl/imgui_impl_glfw.h
    lafez-imgui/impl/imgui_impl_glfw.cpp
    lafez-imgui/impl/imgui_impl_opengl3.h
    lafez-imgui/impl/imgui_impl_opengl3.cpp
)

add_compile_definitions(
    IMGUI_IMPL_OPENGL_LOADER_GLAD
)

target_link_libraries(
    lafez-imgui

    PRIVATE
    glfw
    glad
)

target_include_directories(
    lafez-imgui
    
    PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)