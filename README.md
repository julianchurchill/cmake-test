cmake-test
==========

Build System - Unix Make
------------------------

mkdir build-make
cd build-make
cmake -G "Unix Makefiles" ..
make
make test

Build System - Ninja
--------------------

mkdir build-ninja
cd build-ninja
cmake -G "Ninja" ..
ninja
ninja test

NOTES
-----

- Generated makefiles do depend on the CMakeLists.txt files. This means the makefiles will be auto-generated if the CMakeLists.txt change and the developer only runs 'make'.
- Shared libraries (rather than static) are specified with add_library(name SHARED sourcefiles)

TODO
----

- Building from sub-directories (even if the makefiles have been generated in 'build')
- Incorporating sub-directories that already have their own makefile, e.g. 3rd party components such as the Linux kernel
    - http://www.kitware.com/media/html/BuildingExternalProjectsWithCMake2.8.html
- Avoiding repeated unit test runs if code has not changed (i.e. drop a success file, then subsequently if the dropped file is older than the test executable or dependent libs then rerun the test)
- Cross platform builds (where do the binaries go?)
- Making the 'make test' target check if test exes need a rebuild (the default cmake definition does not depend on the test exes, it simply executes them)
- Try tests with CppUnitLite or another unit test framework

