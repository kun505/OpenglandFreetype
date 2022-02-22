cmake_minimum_required(VERSION 3.0)

project(HELLOFREETYPE)

include_directories(include)

link_directories(lib)

set(LIBS libfreetype.a libpng.so libz.so libbz2.so libglad.a libglfw3.a libGL.so libX11.so libpthread.so libXrandr.so libXi.so libdl.so)
file(GLOB SOURCES "src/*.cpp")
add_executable(main main.cpp ${SOURCES})
target_link_libraries(main ${LIBS})