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

