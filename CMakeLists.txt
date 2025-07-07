cmake_minimum_required(VERSION 3.10)
project(triangles)

set(CMAKE_CXX_STANDARD 17)

file(COPY resources/ DESTINATION ${CMAKE_BINARY_DIR}/resources)

set(RAYLIB_INCLUDE_DIR "${CMAKE_SOURCE_DIR}/include")
set(RAYLIB_LIBRARY "${CMAKE_SOURCE_DIR}/lib/libraylib.a")
set(GLAD_LIBRARY "${CMAKE_SOURCE_DIR}/lib/libglad.a")

add_executable(triangles src/game.cpp)

target_include_directories(triangles PRIVATE 
    ${RAYLIB_INCLUDE_DIR}
)

target_compile_definitions(triangles PRIVATE 
    PLATFORM_DESKTOP
    GRAPHICS_API_OPENGL_33
)

target_link_libraries(triangles 
    ${RAYLIB_LIBRARY}
    ${GLAD_LIBRARY}
    opengl32 
    gdi32 
    winmm 
    user32
    shell32
)
