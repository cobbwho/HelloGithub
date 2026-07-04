# 指定CMake最低版本要求
cmake_minimum_required(VERSION 3.10)

# 设置项目名称和版本
project(HelloGithub VERSION 1.0.0 LANGUAGES CXX)

# 设置语言标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 添加可执行文件
add_executable(${PROJECT_NAME} main.cpp)

target_include_directories(${PROJECT_NAME} PRIVATE 
    ${PROJECT_SOURCE_DIR})

# 设置输出目录（可选）
set_target_properties(${PROJECT_NAME} PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)