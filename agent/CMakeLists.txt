cmake_minimum_required(VERSION 3.10)

add_executable(random_agent random_agent.cpp)

target_link_libraries(random_agent gym jsoncpp curl)
