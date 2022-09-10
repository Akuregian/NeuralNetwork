# CMakeList.txt : CMake project for NeuralNetwork, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

file(GLOB_RECURSE HEADERS "Headers/*.h")
file(GLOB_RECURSE SRC "SOURCE/*.cpp")

# Add source to this project's executable.
add_executable (NeuralNetwork ${HEADERS} ${SRC} "main.cpp")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET NeuralNetwork PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
