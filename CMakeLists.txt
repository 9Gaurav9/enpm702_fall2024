cmake_minimum_required(VERSION 3.20.0)
project(lecture2 VERSION 0.1.0)


# Compilation flags
add_compile_options(-Wall -pedantic-errors)

include_directories(lecture2/include)
# Add executable
add_executable(lecture2 
    lecture2/src/main.cpp lecture2/src/date.cpp
    lecture2/src/engine.cpp)

# add_custom_command(TARGET lecture2 POST_BUILD
#     COMMAND valgrind --show-error-list=yes --leak-check=full --show-leak-kinds=all --track-origins=yes ./lecture2
#     WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}
#     COMMENT "Running Valgrind after building lecture2"
#     VERBATIM
# )


# add_custom_target(run_valgrind ALL
#     COMMAND valgrind --show-error-list=yes --leak-check=full --show-leak-kinds=all --track-origins=yes ./lecture2
#     DEPENDS lecture2
#     WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}
# )


# Set C++ standard to C++17
set_property(TARGET lecture2 PROPERTY CXX_STANDARD 17)

