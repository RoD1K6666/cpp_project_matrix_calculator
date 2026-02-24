cmake_minimum_required(VERSION 3.20)
project(MatrixCalculator LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(matrix
        lib/Matrix.cpp
)
target_include_directories(matrix PUBLIC include)

add_executable(matrix_cli
        src/main.cpp
)
target_link_libraries(matrix_cli PRIVATE matrix)