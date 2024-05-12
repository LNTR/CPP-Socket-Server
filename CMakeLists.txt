cmake_minimum_required(VERSION 3.28)

project(SocketServer)
find_package(Boost COMPONENTS thread REQUIRED)


add_executable(client client.cpp)
add_executable(server server.cpp)

target_link_libraries(server PRIVATE wsock32 ws2_32 ${Boost_LIBRARIES})
target_link_libraries(client PRIVATE wsock32 ws2_32 ${Boost_LIBRARIES})

