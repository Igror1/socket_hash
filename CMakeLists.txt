
cmake_minimum_required(VERSION 3.30)
project(socket_redes)

set(CMAKE_CXX_STANDARD 20)

add_executable(cliente cliente.cpp)

add_executable(servidor servidor.cpp)

# Linka a biblioteca ws2_32 no Windows (Sockets)
if (WIN32)
    target_link_libraries(cliente ws2_32)
    target_link_libraries(servidor ws2_32)
endif()
