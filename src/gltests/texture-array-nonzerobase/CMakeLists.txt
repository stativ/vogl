project(test-texture-array-nonzerobase)
cmake_minimum_required(VERSION 2.8)

include("${SRC_DIR}/build_options.cmake")

aux_source_directory(. SRC_LIST)

add_definitions("-Wno-unused-variable")

add_executable(${PROJECT_NAME} ${SRC_LIST})

target_link_libraries(${PROJECT_NAME}
    SDL2
    ${OPENGL_LIBRARY}
    )

build_options_finalize()

