cmake_minimum_required(VERSION 3.3)

project(boost_function_types)

add_library(boost_function_types INTERFACE)

target_include_directories(boost_function_types BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_function_types DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::function_types ALIAS boost_function_types)
