# gym-http-api(binding-cpp)

C++ binding of [Official package](https://github.com/openai/gym-http-api)
was not easy to use for beginner. 
So, I arrenged those package such as adding CMakeLists.txt and so on.

This package allow you to installing with few steps.

### Installation

1. harumo11/binding-cppをダウンロード
1. Download harumo11/binding-cpp
2. openai/gym-http-api/binding-cppをダウンロードしたファイルで置き換え
2. Replace openai/gym-http-api/binding-cpp directory with harumo11/binding-cpp directory.
3. Build a library controlling OpenAI-Gym from C++.
	```sh
		cd binding-cpp/lib
		mkdir build
		cd build
		cmake ..
		make 
		sudo make install
	```

4. Building a program which uses built library.
	
	```sh
      cd ../agent
      mkdir build
      cd build
      make 
	```
	
5. Checking whether built program can control OpenAI-Gym

	1. Run a OpenAI-Gym server
		
		```sh
		cd opt/gym-http-api
		python3.6 gym_http_server.py
		```
	2. Run a C++ client program
		
		```sh
		cd binding-cpp/agent/build
		./random_agent
		```
