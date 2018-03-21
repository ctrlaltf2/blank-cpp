cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
project(blank-cpp
    LANGUAGES CXX
    DESCRIPTION ""
)

# find_package(Boost 1.65.1 COMPONENTS program_options REQUIRED)

add_executable(blank-cpp
    # src/
)

set_target_properties(blank-cpp
    PROPERTIES
        CXX_STANDARD 11
        CXX_STANDARD_REQUIRED ON
        CXX_EXTENSIONS OFF
        RUNTIME_OUTPUT_DIRECTORY bin
)

target_compile_features(blank-cpp
    PUBLIC
        cxx_std_11
)

target_include_directories(blank-cpp
    PUBLIC
        include
        #        ${Boost_INCLUDE_DIR}
)

target_compile_options(blank-cpp
    PUBLIC
        -Wall
        -Wextra
        -O2
)

#target_link_libraries(blank-cpp
#    PUBLIC
#        ${Boost_LIBRARIES}
#)
