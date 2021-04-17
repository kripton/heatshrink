## Include this file if you want to use the RF24 library
## in YOUR (Pico) project.
## See examples_pico/CMakeLists.txt to see how it could be done

cmake_minimum_required(VERSION 3.12)

# Define the heatshrink library
add_library(heatshrink INTERFACE)

target_sources(heatshrink INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/heatshrink_decoder.c
    ${CMAKE_CURRENT_LIST_DIR}/heatshrink_encoder.c
)

target_include_directories(heatshrink INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/
)
