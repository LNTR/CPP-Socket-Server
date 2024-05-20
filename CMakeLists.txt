cmake_minimum_required(VERSION 3.28)

project(SocketServer)
find_package(Boost COMPONENTS thread REQUIRED)


add_executable(client client-server/client.cpp)
target_link_libraries(client PRIVATE wsock32 ws2_32 ${Boost_LIBRARIES})
set_target_properties(client PROPERTIES RUNTIME_OUTPUT_DIRECTORY client-server)

add_executable(server client-server/server.cpp)
target_link_libraries(server PRIVATE wsock32 ws2_32 ${Boost_LIBRARIES})
set_target_properties(server PROPERTIES RUNTIME_OUTPUT_DIRECTORY client-server)

add_executable(daytime-client daytime-server/daytime-client.cpp)
target_link_libraries(daytime-client PRIVATE wsock32 ws2_32 ${Boost_LIBRARIES})
set_target_properties(daytime-client PROPERTIES RUNTIME_OUTPUT_DIRECTORY daytime-server)


add_executable(daytime-server-sync daytime-server/daytime-server-sync.cpp)
target_link_libraries(daytime-server-sync PRIVATE wsock32 ws2_32 ${Boost_LIBRARIES})
set_target_properties(daytime-server-sync PROPERTIES RUNTIME_OUTPUT_DIRECTORY daytime-server)

add_executable(daytime-server-async daytime-server/daytime-server-async.cpp)
target_link_libraries(daytime-server-async PRIVATE wsock32 ws2_32 ${Boost_LIBRARIES})
set_target_properties(daytime-server-async PROPERTIES RUNTIME_OUTPUT_DIRECTORY daytime-server)


