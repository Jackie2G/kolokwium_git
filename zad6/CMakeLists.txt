cmake_minimum_required(VERSION 3.0)
project(zad6)

include_directories(include)

add_library(dynamiczna SHARED "src/Student.cpp")

add_executable(myProgram "src/libtest.cpp")
target_link_libraries(myProgram dynamiczna)

install(TARGETS myProgram DESTINATION "~/Pulpit/kolokwium_git/zad6/bin")
install(TARGETS dynamiczna DESTINATION "~/Pulpit/kolokwium_git/zad6/lib")
