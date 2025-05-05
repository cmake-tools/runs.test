include(GNUInstallDirs)
add_executable(Main main.cpp)
add_test(NAME Main COMMAND Main)
install(TARGETS Main RUNTIME DESTINATION "${CMAKE_INSTALL_BINDIR}")

add_executable(Main2 main.cpp)
add_test(NAME Main2 COMMAND Main2)
install(TARGETS Main2 RUNTIME DESTINATION "${CMAKE_INSTALL_BINDIR}")

add_executable(Main3 main.cpp)
add_test(NAME Main3 COMMAND Main3)
install(TARGETS Main3 RUNTIME DESTINATION "${CMAKE_INSTALL_BINDIR}")
