cmake_minimum_required(VERSION ${CMAKE_VERSION} FATAL_ERROR)

project(runs.test)

include(CTest)
include(CPack)

message("CMake: ${CMAKE_VERSION}")
message("Generator: ${CMAKE_GENERATOR}")

message(STATUS "Options:")
message(STATUS "\t- source_dir : ${CMAKE_SOURCE_DIR}")
message(STATUS "\t- binary_dir : ${CMAKE_BINARY_DIR}")
message(STATUS "\t- generator : ${CMAKE_GENERATOR}")
message(STATUS "\t- install_prefix : ${CMAKE_INSTALL_PREFIX}")

message(STATUS "\t- BEFORE_CACHE_BOOL : ${BEFORE_CACHE_BOOL}")
message(STATUS "\t- BEFORE_CACHE_STRING : ${BEFORE_CACHE_STRING}")

message(STATUS "\t- AFTER_CACHE_BOOL : ${AFTER_CACHE_BOOL}")
message(STATUS "\t- AFTER_CACHE_STRING : ${AFTER_CACHE_STRING}")

message(AUTHOR_WARNING "I'm a warning")
message(DEPRECATION "I'm a deprecation")

get_cmake_property(_variableNames VARIABLES)
list (SORT _variableNames)
foreach (_variableName ${_variableNames})
    message(STATUS "${_variableName}=${${_variableName}}")
endforeach()


add_subdirectory(src)
