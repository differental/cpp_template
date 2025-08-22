cmake_minimum_required(VERSION 3.25)

project(HelloWorld LANGUAGES CXX)

# C++ Version
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Executable
add_executable(${PROJECT_NAME} src/main.cpp)

# Packages
find_package(fmt CONFIG REQUIRED)

# Link libraries
target_link_libraries(${PROJECT_NAME} PRIVATE fmt::fmt)

# Enable warnings
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_20)
target_compile_options(${PROJECT_NAME} PRIVATE
    $<$<CXX_COMPILER_ID:GNU,Clang>:-Wall -Weffc++ -Wextra -Wconversion -Wsign-conversion -Wpedantic -Werror -Wno-error=effc++>
)

