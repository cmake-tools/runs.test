add_executable(Main main.cpp)
add_test(NAME Main COMMAND Main)

add_executable(Main2 main.cpp)
add_test(NAME Main2 COMMAND Main2)

add_executable(Main3 main.cpp)
add_test(NAME Main3 COMMAND Main3)

install(TARGETS Main Main2 Main3 RUNTIME DESTINATION "${CMAKE_INSTALL_BINDIR}")