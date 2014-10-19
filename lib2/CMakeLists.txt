include_directories(include)

add_library(lib2 SHARED src/lib2.cpp)

add_executable(lib2Test unittest/testmain.cpp)
target_link_libraries(lib2Test lib2)

add_test(lib2Test lib2Test)
