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

TODO
----

- Shared libraries (rather than static)
- Avoiding repeated unit test runs if code has not changed (i.e. drop a success file, then subsequently if the dropped file is older than the test executable or dependent libs then rerun the test)
- Cross platform builds (where do the binaries go?)
- Try tests with CppUnitLite or another unit test framework

