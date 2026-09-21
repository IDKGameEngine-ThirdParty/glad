cmake_minimum_required(VERSION 3.21)

project(glad C)

add_library(
    ${PROJECT_NAME} STATIC ${CMAKE_CURRENT_SOURCE_DIR}/src/glad.c
)
add_library(
    IdkThirdParty::${PROJECT_NAME} ALIAS ${PROJECT_NAME}
)
target_include_directories(
    ${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
)
