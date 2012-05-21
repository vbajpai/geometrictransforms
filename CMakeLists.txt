# ---------------------------------------------------------------------------#
# ------------------------------- CMake -------------------------------------#
# ---------------------------------------------------------------------------#

# minimum supported cmake version
cmake_minimum_required(VERSION 2.6)

# identify the project and programming language
project(gtransforms CXX)

# compiler flags passed as arguments 
add_definitions(-Wall -Werror)

# set output directories for libraries and executables
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

# find external packages
find_package(SDL REQUIRED)

# specify the TARGET executable
add_executable(gtransforms ${CMAKE_SOURCE_DIR}/src/geometrictransforms.cc)

# link external libraries
target_link_libraries(gtransforms ${SDL_LIBRARY})

# ---------------------------------------------------------------------------#
