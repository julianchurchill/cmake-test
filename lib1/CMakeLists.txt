include_directories(include)

add_library(lib1 src/lib1.cpp)

add_executable(lib1Test unittest/testmain.cpp)
target_link_libraries(lib1Test lib1)

add_test(lib1Test lib1Test)
