cmake_minimum_required(VERSION 3.28)
project(CMakeSFMLProject LANGUAGES CXX)

find_package(SFML 3.0.1 REQUIRED COMPONENTS Graphics Audio Window)

add_executable(main main.cpp)
target_compile_features(main PRIVATE cxx_std_17)
target_link_libraries(main PRIVATE  SFML::Graphics SFML::Audio SFML::Window)