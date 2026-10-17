cmake_minimum_required(VERSION 3.26.5)

project(camarero)

include(FetchContent)

FetchContent_Declare(options
    GIT_REPOSITORY https://github.com/estuardoquan/libc.git
    GIT_TAG main
    GIT_SHALLOW TRUE
    SOURCE_SUBDIR options
)

FetchContent_Declare(yaml-cpp
    GIT_REPOSITORY https://github.com/jbeder/yaml-cpp.git
    GIT_TAG yaml-cpp-0.9.0
    GIT_SHALLOW TRUE
)

FetchContent_MakeAvailable(options yaml-cpp)

add_executable(${PROJECT_NAME}
    ./src/main.cpp
    ./src/server_cli.cpp ./src/server_cli.h
    ./src/server_yml.cpp ./src/server_yml.h
    ./src/server.cpp ./src/server.h
)

target_include_directories(${PROJECT_NAME}
    PRIVATE
        ${options_SOURCE_DIR}/options
)

target_link_libraries(${PROJECT_NAME}
    PRIVATE
        options
        yaml-cpp::yaml-cpp
)
