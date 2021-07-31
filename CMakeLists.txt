cmake_minimum_required(VERSION 3.16)
cmake_policy(SET CMP0076 NEW)

# Project and Executable
project(rogue C CXX)
add_executable(${PROJECT_NAME} WIN32 MACOSX_BUNDLE)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_17)

set_target_properties(${PROJECT_NAME} PROPERTIES LINK_FLAGS /SUBSYSTEM:CONSOLE)

add_subdirectory(code)
