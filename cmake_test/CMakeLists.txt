cmake_minimum_required(VERSION 3.15)

project(cmake_test CXX)

set(CMAKE_BUILD_TYPE Debug)

# include(FetchContent)
# FetchContent_Declare(
#   lib-add
#   GIT_REPOSITORY https://github.com/sunjiabin17/cpp_tmp.git
#   GIT_TAG       main
# )
# FetchContent_MakeAvailable(lib-add)

set(VARIABLE1 "VARIABLE1")
message(STATUS "BEFOR subdir: ${VARIABLE1}")
add_subdirectory(cpp_tmp)
message(STATUS "AFTER subdir: ${VARIABLE1}")

# add_executable(main main.cc)

# target_link_libraries(main PRIVATE my_add)
# # target_include_directories(main PRIVATE ${lib-add_SOURCE_DIR}/include)

# include(GNUInstallDirs)
# install(
#   TARGETS main
#   RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
#   LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
#   ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
# )

# get_cmake_property(_variableNames VARIABLES)
# list (SORT _variableNames)
# foreach (_variableName ${_variableNames})
#     message(STATUS "${_variableName}=${${_variableName}}")
# endforeach()
