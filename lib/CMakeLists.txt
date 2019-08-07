cmake_minimum_required(VERSION 3.10)

include_directories(./include)

set(SRC_DIR src)
set(INCLUDE_DIR include/gym)

add_library(gym gym_binding.cpp)
target_link_libraries(gym jsoncpp curl)

install(TARGETS gym
	RUNTIME DESTINATION bin
	LIBRARY DESTINATION lib
	ARCHIVE DESTINATION lib
	)

install(DIRECTORY include/gym
	DESTINATION /usr/local/include
	)
